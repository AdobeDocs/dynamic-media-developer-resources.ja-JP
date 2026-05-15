---
title: setAttr
description: 特定のs7 エレメント IDの任意の属性を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
TQID: 'https://experienceleague.adobe.com/0O1uOLXsh-5PkBnXugpQYJHDAZep49WO3AA4hjClODk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 1%

---

# setAttr{#setattr}

特定のs7:elementIDの任意の属性を設定します。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXG ノード要素に`s7:elementID`が定義されている場合は、そのノードの属性を操作できます。 必要な数の属性/値ペアを設定できます。 属性は、FXGで既に定義されている必要はありませんが、ノード要素に対して有効である必要があります。 `{}`の間のすべての値はエスケープする必要があります。

## 例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

`s7:elementID="Group1"`属性が`BitmapGraphic` ノードに対して定義されていると仮定すると、次は有効です。

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

この例では、`BitmapGraphic`に&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*&#x200B;および&#x200B;*[!DNL scaleY]*&#x200B;を設定し、既存の値をすべて上書きします。
