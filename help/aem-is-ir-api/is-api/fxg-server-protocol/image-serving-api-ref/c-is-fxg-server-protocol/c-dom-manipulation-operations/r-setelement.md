---
description: XMLをs7 elementIDに設定します。
solution: Experience Manager
title: setElement
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
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
