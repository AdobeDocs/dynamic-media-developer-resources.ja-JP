---
title: setElement
description: XMLをs7 elementIDに設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
TQID: 'https://experienceleague.adobe.com/bLej-B1yRcTdFFXhaigx4Zf9ubwx9LkR31a9Rqdr0Zs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 62
ht-degree: 1%

---

# setElement{#setelement}

XMLをs7:elementIDに設定します。

`setElement.elementID=<XML>`

FXG ノード要素に`s7:elementID`が定義されている場合、`<XML>`値は子要素として置き換えられます。 `<XML>`はエンコードする必要があります。

## 例 {#section-f23a998b18994dd3b5d4e1965718db9f}

`s7:elementID="group2"`属性が`Group` ノードに対して定義されていると仮定すると、次は有効です。

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の使用例は、すべての子ノードを`group2` ノードから削除し、新しい`TextGraphic`子ノードに置き換えます。
