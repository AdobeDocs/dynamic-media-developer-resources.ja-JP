---
description: 指定したs7 elementIDの任意の属性を設定します。
seo-description: 指定したs7 elementIDの任意の属性を設定します。
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAttr{#setattr}

指定したs7:elementIDの任意の属性を設定します。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXGノード要素に定義済みの要素があ `s7:elementID` る場合は、そのノードの属性を操作できます。 属性/値のペアは必要な数だけ設定できます。 属性をFXGで既に定義する必要はありませんが、ノード要素に対して有効である必要があります。 間の値はすべてエスケープ `{}` する必要があります。

## 例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

ノードに対し `s7:elementID="Group1"` て属性が定義されてい `BitmapGraphic` る場合、次の値が有効であるとします。

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

次の使用例は、、、、、お *[!DNL x]*&#x200B;よびの値を設 *[!DNL y]*&#x200B;定し、 *[!DNL rotation]*&#x200B;既存の値を *[!DNL scaleX]**[!DNL scaleY]*`BitmapGraphic` 上書きします。
