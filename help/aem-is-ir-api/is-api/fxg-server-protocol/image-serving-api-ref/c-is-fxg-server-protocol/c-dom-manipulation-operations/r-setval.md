---
description: s7 elementIDのテキストノード値を設定します。
seo-description: s7 elementIDのテキストノード値を設定します。
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
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
