---
description: マテリアルカタログは、多くのイメージレンダリング設定を提供します。
solution: Experience Manager
title: マテリアルカタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# マテリアルカタログ{#material-catalogs}

マテリアルカタログは、多くのイメージレンダリング設定を提供します。

マテリアルカタログは、実際のファイルパスへの要求で使用されるビネットとマテリアル ID をマッピングし、マテリアルに関連付けられたすべてのメタデータを保存し、テンプレート用のコンテナを提供できます。 ICC プロファイルとコマンドマクロを追跡します。

マテリアルカタログは、画像レンダリングの Java コンポーネント ( [!DNL Platform Server]) をクリックします。 カタログ属性ファイルには [!DNL .ini] サフィックスを付けて、登録済みのカタログフォルダ ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)) をクリックします。 既定のマテリアルカタログ ( [!DNL default.ini]) が常に存在し、画像サービングを正しく機能させるには、すべての属性を設定する必要があります。
