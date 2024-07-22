---
title: setAttr
description: 特定の s7 要素 ID に任意の属性を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

指定された s7:elementID に任意の属性を設定します。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXG ノード要素に `s7:elementID` が定義されている場合は、そのノードのアトリビュートを操作できます。 属性と値のペアは、必要なだけ設定できます。 属性は、FXG ですでに定義されている必要はありませんが、ノード要素に対して有効である必要があります。 `{}` の間のすべての値はエスケープする必要があります。

## 例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

`BitmapGraphic` ノードに対して `s7:elementID="Group1"` 属性が定義されているとすると、次の属性は有効です。

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

この例では、`BitmapGraphic` の *[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]* および *[!DNL scaleY]* を設定し、既存の値を上書きします。
