---
description: s7 elementIDのテキストノード値を設定します。
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

s7:elementIDのテキストノード値を設定します。

`setVal.elementID= *[!DNL value]*`

FXGノード要素に`s7:elementID`が定義されている場合は、そのノードのテキスト値を操作できます。

## 例 {#section-f574fd66dedd4a219aa537d7bdabea23}

`s7:elementID="paragraph1"`属性が`TextGraphic`ノードに対して定義されている場合、次の値が有効であるとします。

`&setVal.paragraph=Hello`

次の使用例は、段落ノードのテキスト値を「Hello」に設定します。
