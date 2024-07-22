---
description: マテリアル カタログには、多くのイメージ レンダリング環境設定が用意されています。
solution: Experience Manager
title: 材料カタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 材料カタログ{#material-catalogs}

マテリアル カタログには、多くのイメージ レンダリング環境設定が用意されています。

マテリアル カタログは、リクエストで使用されるビネットとマテリアル ID を実際のファイル パスにマッピングし、マテリアルに関連付けられたすべてのメタデータを保存して、テンプレートのコンテナを提供できます。 ICC プロファイルとコマンドマクロを追跡します。

マテリアルカタログには、画像レンダリングの Java コンポーネント（と [!DNL Platform Server] 連配置）でのみアクセスできます。 カタログ属性ファイルには [!DNL .ini] の接尾辞を付け、登録されたカタログフォルダー（[ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)）に配置する必要があります。 デフォルトの素材カタログ（[!DNL default.ini]）は常に存在し、画像サービングが正しく機能するようにすべての属性を入力する必要があります。
