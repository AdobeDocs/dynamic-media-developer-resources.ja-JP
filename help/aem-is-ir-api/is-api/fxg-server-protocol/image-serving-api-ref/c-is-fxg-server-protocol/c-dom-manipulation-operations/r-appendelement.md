---
title: appendElement
description: s7elementID に XML を追加します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# appendElement{#appendelement}

s7:elementID に XML を追加します。

`appendElement.elementID=<XML>`

FXG ノード要素に `s7:elementID` 定義済み、 `<XML>` の値が子要素として追加されます。 The `<XML>` はエンコードする必要があります。

## 例 {#section-4368570aa198485d91b73b4d0741478f}

次を想定する： `s7:elementID="group1"` 属性が Group ノードに対して定義されている場合、次の値が有効です。

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の使用例は、テキストグラフィックの子をに追加します。 `group1`.
