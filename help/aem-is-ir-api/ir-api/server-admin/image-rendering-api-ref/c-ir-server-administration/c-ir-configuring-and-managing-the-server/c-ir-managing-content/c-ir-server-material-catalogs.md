---
description: マテリアルカタログには、多くのイメージレンダリング設定が用意されています。
seo-description: マテリアルカタログには、多くのイメージレンダリング設定が用意されています。
seo-title: マテリアルカタログ
solution: Experience Manager
title: マテリアルカタログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# マテリアルカタログ{#material-catalogs}

マテリアルカタログには、多くのイメージレンダリング設定が用意されています。

マテリアルカタログは、要求で使用されるビネットとマテリアルIDを実際のファイルパスにマッピングし、マテリアルに関連付けられたすべてのメタデータを保存し、テンプレートのコンテナを提供します。 ICCプロファイルとコマンドマクロを追跡します。

マテリアルカタログは、イメージレンダリングのJavaコンポーネント（プラットフォームサーバと共に配置）からのみアクセスできます。 カタログ属性ファイルには[!DNL .ini]サフィックスが必要で、登録済みのカタログフォルダー([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))に配置します。 初期設定のマテリアルカタログ([!DNL default.ini])は常に存在し、画像サービングを正しく機能させるために、すべての属性を設定する必要があります。
