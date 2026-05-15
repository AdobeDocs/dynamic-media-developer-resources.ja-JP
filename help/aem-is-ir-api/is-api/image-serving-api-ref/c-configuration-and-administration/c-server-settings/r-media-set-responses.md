---
title: メディアセットの応答
description: このセクションの設定は、req=set修飾子によって取得されたメディアセット応答に適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: 'https://experienceleague.adobe.com/FNUguOqf8f5FnIeGTzheZU-8zCXqwRMU3YGyvYDA0uM'
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
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# メディアセットの応答{#media-set-responses}

このセクションの設定は、`req=set`修飾子によって取得されたメディアセット応答に適用されます。

## PS::fvctx.useCatalogRecordValidation - Caching Policy {#section-9accb087d16548a988993bb30395a6f6}

このプロパティは、キャッシュから取得したset応答を再生成する必要があるかどうかを判断する際に、キャッシュポリシーを制御します。 プロパティが無効になっている場合、[!DNL catalog.ini] ファイルのタイムスタンプが検証に使用されます。 プロパティが有効になっている場合、すべての参照レコードの最新の`catalog::LastModified` タイムスタンプが検証に使用されます。

## PS::fvctx.nestingLimit - Nesting Limit {#section-280210341f1647fea02590e7069934d2}

任意の`req=set`応答の最大ネスト深度。 この深度を超えると、エラーが返されます。

## PS::fvctx.brochureLimit - パンフレットの制限 {#section-fe36e47db49244cea7f07e9dd3639440}

関連付けられたすべてのメタデータを含む、`req=set`応答の電子カタログパンフレットの最大数。 この制限を超えると、パンフレット項目に関連付けられているプライベートマップとユーザーデータは除外されます。
