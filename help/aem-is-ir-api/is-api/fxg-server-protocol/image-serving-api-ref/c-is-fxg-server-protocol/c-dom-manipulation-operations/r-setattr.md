---
title: setAttr
description: 指定された s7 elementID に任意の属性を設定します。
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

指定した s7:elementID の任意の属性を設定します。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXG ノード要素に `s7:elementID` 定義済みの場合は、そのノードのアトリビュートを操作できます。 属性と値のペアは必要な数だけ設定できます。 属性を FXG で既に定義している必要はありませんが、ノード要素に対して有効である必要があります。 範囲内のすべての値 `{}` はエスケープする必要があります。

## 例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

次を想定する： `s7:elementID="Group1"` 属性が `BitmapGraphic` ノードの場合、次の値が有効です。

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

次の例では、 *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*、および *[!DNL scaleY]* （の） `BitmapGraphic` およびは、既存の値を上書きします。
