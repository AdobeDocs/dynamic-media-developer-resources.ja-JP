---
description: マテリアルカタログには、多くの画像レンダリング設定が用意されています。
solution: Experience Manager
title: マテリアルカタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# マテリアルカタログ{#material-catalogs}

マテリアルカタログには、多くの画像レンダリング設定が用意されています。

マテリアルカタログ リクエストで使用されるビネットとマテリアル IDを実際のファイルパスにマッピングし、マテリアルに関連するすべてのメタデータを保存し、テンプレート用のコンテナを提供できます。 彼らはICC プロファイルとコマンドマクロを追跡します。

マテリアルカタログには、画像レンダリングのJava コンポーネント（[!DNL Platform Server]と同じ場所）によってのみアクセスできます。 カタログ属性ファイルには[!DNL .ini]のサフィックスを付け、登録されたカタログフォルダー（[ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)）に配置する必要があります。 既定のマテリアル カタログ（[!DNL default.ini]）は常に存在する必要があり、画像サービングを正しく機能させるためにすべての属性を入力する必要があります。

