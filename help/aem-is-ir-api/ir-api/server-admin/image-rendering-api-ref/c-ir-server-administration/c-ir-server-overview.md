---
description: このドキュメントでは、Scene7 Image Rendering Serverの管理方法を説明します。
seo-description: このドキュメントでは、Scene7 Image Rendering Serverの管理方法を説明します。
seo-title: サーバー管理の概要
solution: Experience Manager
title: サーバー管理の概要
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# サーバー管理の概要{#server-administration-overview}

このドキュメントでは、Scene7 Image Rendering Serverの管理方法を説明します。

イメージレンダリングは、次の2つの主要なコンポーネントで構成されます。

* Javaパッケージは、Image Serving Platform Serverと共にデプロイされ、クライアント接続、キャッシュ、マテリアルカタログを管理します。
* ネイティブコードモジュールは、Image Serverの拡張ライブラリとしてデプロイされ、コアイメージレンダリング機能を実装します。

両方のコンポーネントをまとめて *Render Serverと呼びます*。

画像レンダリングは、多くのサーバ機能と画像サービングを共有し、すべてのオプションは設定ファイルを編集することで設定します。 追加の設定属性は、既定のカタログ()または特定のマテ [!DNL default.ini]リアルカタログによって提供されます。 詳しくは、マテリアルカタログを参照してください。

イメージレンダリングのインスト *[!DNL install_folder]*&#x200B;ールフォルダ()は[!DNL *[!DNL install_root]*/ImageRendering]です。 Windowsの場合、デフォルトは *[!DNL install_root]* です `C:\Program Files\Scene7`。 インストール時に別のフォルダーを指定できます。 Linuxでは、常に *[!DNL install_root]* が必要です [!DNL /usr/local/scene7]。 シンボリックリンクを使用できます。

UNIXではすべてのファイルパスで大文字と小文字が区別され、Windowsでは大文字と小文字が区別されません。
