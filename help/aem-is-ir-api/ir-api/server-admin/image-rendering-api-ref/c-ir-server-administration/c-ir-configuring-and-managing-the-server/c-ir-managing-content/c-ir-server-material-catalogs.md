---
description: マテリアルカタログは、多くのイメージレンダリング設定を提供します。
seo-description: マテリアルカタログは、多くのイメージレンダリング設定を提供します。
seo-title: マテリアルカタログ
solution: Experience Manager
title: マテリアルカタログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# マテリアルカタログ{#material-catalogs}

マテリアルカタログは、多くのイメージレンダリング設定を提供します。

マテリアルカタログは、実際のファイルパスへの要求で使用されるビネットとマテリアルIDをマッピングし、マテリアルに関連付けられたすべてのメタデータを保存し、テンプレートのコンテナを提供します。 ICCプロファイルとコマンドマクロを追跡します。

マテリアルカタログは、イメージレンダリングのJavaコンポーネント（プラットフォームサーバと共に配置）によってのみアクセスされます。 カタログ属性ファイルは、サフィッ [!DNL .ini] クスを持ち、登録済みのカタログフォルダ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))に配置する必要があります。 画像サービングを正しく機能させるには、初期設定のマテ [!DNL default.ini]リアルカタログ()が常に存在し、すべての属性を設定している必要があります。
