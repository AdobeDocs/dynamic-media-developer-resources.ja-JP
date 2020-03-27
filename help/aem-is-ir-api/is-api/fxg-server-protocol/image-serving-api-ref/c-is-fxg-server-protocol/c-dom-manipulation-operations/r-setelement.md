---
description: XMLをs7elementIDに設定します。
seo-description: XMLをs7elementIDに設定します。
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

XMLをs7:elementIDに設定します。

`setElement.elementID=<XML>`

FXGノード要素が定義されてい `s7:elementID` る場合、値 `<XML>` は子要素として置き換えられます。 The `<XML>` must be encoded.

## 例 {#section-f23a998b18994dd3b5d4e1965718db9f}

ノードに対し `s7:elementID="group2"` て属性が定義されてい `Group` る場合、次の値が有効であるとします。

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の例では、ノードからすべての子を削 `group2`除し、新しい子ノードに置き換 `TextGraphic` えます。
