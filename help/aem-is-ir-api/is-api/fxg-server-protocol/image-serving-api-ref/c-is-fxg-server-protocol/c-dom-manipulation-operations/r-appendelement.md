---
description: s7elementIDにXMLを追加します。
solution: Experience Manager
title: appendElement
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# appendElement{#appendelement}

XMLをs7:elementIDに追加します。

`appendElement.elementID=<XML>`

FXGノード要素で`s7:elementID`が定義されている場合、`<XML>`値は子要素として追加されます。 `<XML>`はエンコードする必要があります。

## 例 {#section-4368570aa198485d91b73b4d0741478f}

`s7:elementID="group1"`属性がグループノードに対して定義されている場合、次の値が有効であるとします。

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の使用例は、テキストグラフィックの子を`group1`に追加します。
