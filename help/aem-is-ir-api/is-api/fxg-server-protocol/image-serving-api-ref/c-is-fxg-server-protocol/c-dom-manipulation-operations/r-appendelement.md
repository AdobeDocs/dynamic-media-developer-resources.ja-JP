---
title: appendElement
description: s7要素IDにXMLを追加します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
TQID: 'https://experienceleague.adobe.com/6MrVZiak-nj9nJgDpd5GBcVwd9vbn86pCSxIUTiHTxU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 1%

---

# appendElement{#appendelement}

s7:elementIDにXMLを追加します。

`appendElement.elementID=<XML>`

FXG ノード要素に`s7:elementID`が定義されている場合、`<XML>`値は子要素として追加されます。 `<XML>`はエンコードする必要があります。

## 例 {#section-4368570aa198485d91b73b4d0741478f}

`s7:elementID="group1"`属性がグループ ノードに対して定義されていると仮定すると、次は有効です。

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

この例では、テキストグラフィックの子を`group1`に追加します。
