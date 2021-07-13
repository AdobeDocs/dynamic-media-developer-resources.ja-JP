---
description: s7elementIDにXMLを追加する。
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# appendElement{#appendelement}

s7:elementIDにXMLを追加する。

`appendElement.elementID=<XML>`

FXGノード要素に`s7:elementID`が定義されている場合、`<XML>`値が子要素として追加されます。 `<XML>`はエンコードする必要があります。

## 例 {#section-4368570aa198485d91b73b4d0741478f}

`s7:elementID="group1"`属性がグループノードに対して定義され、次の属性が有効であるとします。

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の使用例は、テキストグラフィック子を`group1`に追加します。
