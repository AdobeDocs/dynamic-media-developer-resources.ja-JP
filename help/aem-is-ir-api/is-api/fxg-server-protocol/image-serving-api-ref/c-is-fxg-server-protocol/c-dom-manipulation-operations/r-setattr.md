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
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# setAttr{#setattr}

指定したs7:elementIDの任意の属性を設定します。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXGノード要素に`s7:elementID`が定義されている場合は、そのノードの属性を操作できます。 属性/値のペアは必要な数だけ設定できます。 属性はFXGで既に定義する必要はありませんが、ノード要素に対して有効である必要があります。 `{}`の範囲内の値はすべてエスケープする必要があります。

## 例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

`s7:elementID="Group1"`属性が`BitmapGraphic`ノードに対して定義されている場合、次の値が有効であるとします。

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

次の例では、`BitmapGraphic`に&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*、*[!DNL scaleY]*&#x200B;を設定し、既存の値を上書きします。
