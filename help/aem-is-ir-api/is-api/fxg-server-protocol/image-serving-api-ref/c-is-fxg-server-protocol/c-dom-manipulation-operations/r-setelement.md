---
description: XMLをs7 elementIDに設定します。
seo-description: XMLをs7 elementIDに設定します。
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---


# setElement{#setelement}

XMLをs7:elementIDに設定します。

`setElement.elementID=<XML>`

FXGノード要素で`s7:elementID`が定義されている場合、`<XML>`値は子要素として置き換えられます。 `<XML>`はエンコードする必要があります。

## 例 {#section-f23a998b18994dd3b5d4e1965718db9f}

`s7:elementID="group2"`属性が`Group`ノードに対して定義されている場合、次の値が有効であるとします。

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の例では、`group2`ノードからすべての子を削除し、新しい`TextGraphic`子ノードに置き換えます。
