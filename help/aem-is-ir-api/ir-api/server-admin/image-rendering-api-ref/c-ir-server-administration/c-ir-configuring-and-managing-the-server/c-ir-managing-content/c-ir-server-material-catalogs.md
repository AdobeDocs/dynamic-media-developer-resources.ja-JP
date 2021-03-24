---
description: マテリアルカタログには、多くのイメージレンダリング設定が用意されています。
solution: Experience Manager
title: マテリアルカタログ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# マテリアルカタログ{#material-catalogs}

マテリアルカタログには、多くのイメージレンダリング設定が用意されています。

マテリアルカタログは、要求で使用されるビネットとマテリアルIDを実際のファイルパスにマッピングし、マテリアルに関連付けられたすべてのメタデータを保存し、テンプレートのコンテナを提供します。 ICCプロファイルとコマンドマクロを追跡します。

マテリアルカタログは、イメージレンダリングのJavaコンポーネント（プラットフォームサーバと共に配置）からのみアクセスできます。 カタログ属性ファイルには[!DNL .ini]サフィックスが必要で、登録済みのカタログフォルダー([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))に配置します。 初期設定のマテリアルカタログ([!DNL default.ini])は常に存在し、画像サービングを正しく機能させるために、すべての属性を設定する必要があります。
