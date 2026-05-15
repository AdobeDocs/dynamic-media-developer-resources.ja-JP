---
title: setVal
description: s7 elementIDのテキストノード値を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
TQID: 'https://experienceleague.adobe.com/bwE12rWee56rVQDuctPsmq5TUwVJy39HNUff-ZYuybM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 1%

---

# setVal{#setval}

s7:elementIDのテキストノード値を設定します。

`setVal.elementID= *[!DNL value]*`

FXG ノード要素に`s7:elementID`が定義されている場合、そのノードのテキスト値を操作できます。

## 例 {#section-f574fd66dedd4a219aa537d7bdabea23}

`s7:elementID="paragraph1"`属性が`TextGraphic` ノードに対して定義されていると仮定すると、次は有効です。

`&setVal.paragraph=Hello`

次の使用例は、段落ノードのテキスト値を「Hello」に設定します。
