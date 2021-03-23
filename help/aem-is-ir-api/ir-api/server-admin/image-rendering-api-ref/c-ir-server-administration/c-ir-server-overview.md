---
description: このドキュメントでは、Dynamic Mediaイメージレンダリングサーバの管理方法を説明します。
seo-description: このドキュメントでは、Dynamic Mediaイメージレンダリングサーバの管理方法を説明します。
seo-title: サーバー管理の概要
solution: Experience Manager
title: サーバー管理の概要
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# サーバ管理の概要{#server-administration-overview}

このドキュメントでは、Dynamic Mediaイメージレンダリングサーバの管理方法を説明します。

イメージレンダリングは、次の2つの主要なコンポーネントで構成されています。

* JavaパッケージはImage Serving Platform Serverと共にデプロイされ、クライアント接続、キャッシュ、マテリアルカタログを管理します。
* ネイティブコードモジュールは、Image Serverの拡張ライブラリとしてデプロイされ、コアの画像レンダリング機能を実装します。

両方のコンポーネントをまとめて&#x200B;*Render Server*&#x200B;と呼びます。

画像レンダリングは、画像サービングと多くのサーバ機能を共有し、すべてのオプションは設定ファイルを編集することで設定します。 追加の設定属性は、デフォルトのカタログ([!DNL default.ini])または特定のマテリアルカタログで提供されます。 詳細は、「マテリアルカタログ」を参照してください。

イメージレンダリングインストールフォルダー(*[!DNL install_folder]*)は[!DNL *[!DNL install_root]*/ImageRendering]です。 Windowsの場合、デフォルトの&#x200B;*[!DNL install_root]*&#x200B;は`C:\Program Files\Scene7`です。 インストール時に別のフォルダーを指定することができます。 Linuxでは、*[!DNL install_root]*&#x200B;は常に[!DNL /usr/local/scene7]でなければなりません。 シンボリックリンクを使用できます。

UNIXでは、すべてのファイルパスで大文字と小文字が区別され、Windowsでは大文字と小文字が区別されません。
