---
description: このドキュメントでは、Dynamic Media Image Renderingサーバーの管理方法を説明します。
solution: Experience Manager
title: サーバー管理の概要
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# サーバー管理の概要{#server-administration-overview}

このドキュメントでは、Dynamic Media Image Renderingサーバーの管理方法を説明します。

画像レンダリングは、次の2つの主要なコンポーネントで構成されます。

* JavaパッケージはImage Serving Platform Serverと共にデプロイされ、クライアント接続、キャッシュ、マテリアルカタログを管理します。
* ネイティブコードモジュールは、Image Serverの拡張機能ライブラリとしてデプロイされ、主な画像レンダリング機能を実装します。

両方のコンポーネントをまとめて&#x200B;*レンダーサーバ*&#x200B;と呼びます。

画像レンダリングは、画像サービングと多くのサーバ機能を共有します。すべてのオプションは設定ファイルを編集することで設定されます。 追加の設定属性は、既定のカタログ( [!DNL default.ini] )または特定のマテリアルカタログで提供されます。 詳細は、マテリアルカタログを参照してください。

画像レンダリングのインストールフォルダー(*[!DNL install_folder]*)は[!DNL *[!DNL install_root]*/ImageRendering]です。 Windowsの場合、デフォルトの&#x200B;*[!DNL install_root]*&#x200B;は`C:\Program Files\Scene7`です。 インストール中に別のフォルダーを指定することもできます。 Linuxでは、*[!DNL install_root]*&#x200B;は常に[!DNL /usr/local/scene7]である必要があります。 シンボリックリンクを使用できます。

UNIXではすべてのファイル・パスで大文字と小文字が区別され、Windowsでは大文字と小文字が区別されません。
