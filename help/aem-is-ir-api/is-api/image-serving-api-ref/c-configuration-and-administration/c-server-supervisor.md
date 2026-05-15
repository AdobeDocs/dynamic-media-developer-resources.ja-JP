---
description: Image Serving コンポーネントは、サーバースーパーバイザー（Linux デーモンまたはWindows サービス）によって管理されます（S7Supervisor.exe、サービスCampaign コントロールパネルの「Dynamic Media Image Serving」に記載）。
solution: Experience Manager
title: サーバースーパーバイザー
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
TQID: 'https://experienceleague.adobe.com/D3cGGQLVly7MwWSvSjkWcWkuR9kVUFC9sSvItZm6eOc'
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
source-wordcount: 138
ht-degree: 0%

---

# サーバースーパーバイザー{#server-supervisor}

Image Serving コンポーネントは、サーバースーパーバイザー（Linux デーモンまたはWindows サービス）によって管理されます（S7Supervisor.exe、サービスCampaign コントロールパネルの「Dynamic Media Image Serving」に記載）。

サーバースーパーバイザーは、他の画像サービスコンポーネントの開始と停止に加えて、これらの他のコンポーネントの健全性を確保する責任があります。 コンポーネントがクラッシュした場合は、サービスの中断を最小限に抑えるために自動的に再起動されます。

## 開始と停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

サーバースーパーバイザーは、Image Serving ユーティリティスクリプトを使用して起動、停止、再起動します。 詳しくは、[&#x200B; ユーティリティのドキュメント &#x200B;](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)を参照してください。

サーバースーパーバイザの起動と停止は、その他のすべてのImage Serving コンポーネントを自動的に起動および停止します。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
