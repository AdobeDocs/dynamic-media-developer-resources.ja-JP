---
description: 指定したs7 elementIDの属性を設定します。
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setAttr{#setattr}

指定したs7:elementIDの属性を設定します。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXGノード要素に`s7:elementID`が定義されている場合は、そのノードの属性を操作できます。 属性/値のペアは必要な数だけ設定できます。 属性は、FXGで既に定義されている必要はありませんが、ノード要素に対して有効である必要があります。 `{}`の間の値はすべてエスケープする必要があります。

## 例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

`s7:elementID="Group1"`属性が`BitmapGraphic`ノードに対して定義されている場合、次の値が有効です。

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

この例では、`BitmapGraphic`に&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*&#x200B;および&#x200B;*[!DNL scaleY]*&#x200B;を設定し、既存の値を上書きします。
