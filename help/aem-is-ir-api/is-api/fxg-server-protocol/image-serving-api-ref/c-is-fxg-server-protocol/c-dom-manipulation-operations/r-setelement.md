---
description: XMLをs7elementIDに設定します。
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# setElement{#setelement}

XMLをs7:elementIDに設定します。

`setElement.elementID=<XML>`

FXGノード要素に`s7:elementID`が定義されている場合、`<XML>`値は子要素として置き換えられます。 `<XML>`はエンコードする必要があります。

## 例 {#section-f23a998b18994dd3b5d4e1965718db9f}

`s7:elementID="group2"`属性が`Group`ノードに対して定義され、次の値が有効であるとします。

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の例では、`group2`ノードからすべての子を削除し、新しい`TextGraphic`子ノードに置き換えます。
