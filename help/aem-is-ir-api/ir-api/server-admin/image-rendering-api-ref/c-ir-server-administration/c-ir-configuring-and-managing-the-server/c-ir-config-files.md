---
description: 画像レンダリングの設定設定は、 [!DNL Platform Server] 設定ファイルに保存されます。
solution: Experience Manager
title: 設定ファイル
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: 'https://experienceleague.adobe.com/KTBXtuSOstPMi7bPQg70jyUVCqcXlLiLPiFFhyp9iFg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# 設定ファイル{#configuration-files}

画像レンダリングの設定設定は、[!DNL Platform Server]設定ファイルに保存されます。

プラットフォームサーバー設定ファイルは[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]にあります。 このファイルはJAVA プロパティファイルです。 適切な規則に従うように注意を払う必要があります。そうしないと、[!DNL Platform Server]を開始できない可能性があります。 Windows ファイルパスでは、単純なバックスラッシュ （\）ではなく、ダブルバックスラッシュ （`\\`）または1つのフォワードスラッシュ （/）を使用する必要があります。これは、バックスラッシュがこのタイプのファイルではエスケープ文字として使用されるためです。 このファイルには、内部サーバーで使用する文書化されていないプロパティが含まれており、変更することはできません。

すべての画像レンダリング設定の一覧については、[構成設定リファレンス &#x200B;](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)を参照してください。
