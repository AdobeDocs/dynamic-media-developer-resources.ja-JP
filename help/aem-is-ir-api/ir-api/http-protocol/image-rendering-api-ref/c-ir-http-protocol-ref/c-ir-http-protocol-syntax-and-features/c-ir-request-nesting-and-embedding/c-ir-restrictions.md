---
title: 制限
description: ネストと埋め込みには、いくつかの制限が適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# 制限{#restrictions}

ネストと埋め込みには、いくつかの制限が適用されます。

サーバーのパフォーマンスを高めるために、ネストされたリクエストによって返される画像の解像度は、マテリアルが適用されるオブジェクトのテクスチャ解像度と合理的に一致する必要があります。

外部イメージはローカルにキャッシュされます。 そのような画像への変更は、ローカルキャッシュエントリが古くなった後にのみ検出されます（有効期限HTTP ヘッダーに基づいて）。

