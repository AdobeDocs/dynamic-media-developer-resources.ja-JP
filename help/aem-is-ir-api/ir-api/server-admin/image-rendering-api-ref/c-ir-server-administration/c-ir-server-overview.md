---
description: このドキュメントでは、Dynamic Media Image Rendering サーバーの管理方法を説明します。
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

このドキュメントでは、Dynamic Media Image Rendering サーバーの管理方法を説明します。

画像レンダリングは、次の 2 つの主要なコンポーネントで構成されます。

* Java パッケージは画像サービングと共にデプロイされます [!DNL Platform Server] およびは、クライアント接続、キャッシュ、マテリアルカタログを管理します。
* ネイティブコードモジュールは、Image Server の拡張ライブラリとしてデプロイされ、コアの画像レンダリング機能を実装します。

両方のコンポーネントをまとめて *Render Server*.

画像レンダリングは、多くのサーバ機能を画像サービングと共有し、すべてのオプションは設定ファイルを編集することで設定します。 追加の設定属性は、デフォルトのカタログ ( [!DNL default.ini]) または特定のマテリアルカタログ 詳細は、マテリアルカタログを参照してください。

Image Rendering のインストールフォルダー ( *[!DNL install_folder]*) は [!DNL *[!DNL install_root]*/ImageRendering] を呼び出します。 Windows の場合、デフォルトは *[!DNL install_root]* が `C:\Program Files\Scene7`. インストール時に別のフォルダを指定することもできます。 Linux の場合、 *[!DNL install_root]* は常に [!DNL /usr/local/scene7]. シンボリックリンクを使用できます。

UNIX ではすべてのファイル・パスで大文字と小文字が区別され、Windows では大文字と小文字が区別されません。
