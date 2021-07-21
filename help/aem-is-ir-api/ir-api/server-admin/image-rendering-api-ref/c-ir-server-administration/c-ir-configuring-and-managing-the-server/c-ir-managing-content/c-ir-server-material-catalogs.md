---
description: マテリアルカタログは、多くのイメージレンダリング設定を提供します。
solution: Experience Manager
title: マテリアルカタログ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# マテリアルカタログ{#material-catalogs}

マテリアルカタログは、多くのイメージレンダリング設定を提供します。

マテリアルカタログは、実際のファイルパスへのリクエストで使用されるビネットとマテリアルIDをマップし、マテリアルに関連付けられたすべてのメタデータを保存し、テンプレート用のコンテナを提供します。 ICCプロファイルとコマンドマクロを追跡します。

マテリアルカタログは、画像レンダリングのJavaコンポーネント（Platform Serverと共に配置）によってのみアクセスされます。 カタログ属性ファイルには[!DNL .ini]サフィックスが付き、登録済みのカタログフォルダー([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))に配置されている必要があります。 画像サービングを正しく機能させるには、デフォルトのマテリアルカタログ([!DNL default.ini])が常に存在し、すべての属性を設定する必要があります。
