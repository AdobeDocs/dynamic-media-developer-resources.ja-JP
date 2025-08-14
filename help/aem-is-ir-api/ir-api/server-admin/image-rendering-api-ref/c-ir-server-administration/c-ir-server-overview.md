---
description: このドキュメントでは、Dynamic Media 画像レンダリングサーバーの管理方法について説明します。
solution: Experience Manager
title: サーバー管理の概要
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# サーバー管理の概要{#server-administration-overview}

このドキュメントでは、Dynamic Media 画像レンダリングサーバーの管理方法について説明します。

画像レンダリングは、次の 2 つの主要コンポーネントで構成されます。

* Java パッケージは、画像サービングサー [!DNL Platform Server] スと共にデプロイされ、クライアント接続、キャッシュ、マテリアルカタログを管理します。
* ネイティブコードモジュールは、Image Server の拡張機能ライブラリとしてデプロイされ、コア画像レンダリング機能を実装します。

両方のコンポーネントをまとめて *Render Server* と呼びます。

画像レンダリングは、多くのサーバー機能を画像サービングと共有し、すべてのオプションは設定ファイルを編集することで設定されます。 追加の設定属性は、既定のカタログ（[!DNL default.ini]）または特定の材料カタログによって提供されます。 詳細については、「マテリアル カタログ」を参照してください。

画像レンダリングのインストールフォルダー（*[!DNL install_folder]*）は [!DNL *[!DNL install_root]*/ImageRendering] です。 Windows の場合、デフォルト *[!DNL install_root]* は `C:\Program Files\Scene7` です。 インストール時に別のフォルダーを指定することもできます。 Linux の場合、*[!DNL install_root]* は常に [!DNL /usr/local/scene7] である必要があります。 シンボリックリンクを使用できます。

すべてのファイルパスは、UNIX では大文字と小文字が区別され、Windows では大文字と小文字が区別されません。
