---
description: s7elementIDのテキストノード値を設定します。
seo-description: s7elementIDのテキストノード値を設定します。
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setVal{#setval}

s7:elementIDのテキストノード値を設定します。

`setVal.elementID= *[!DNL value]*`

FXGノード要素に定義済みの値が `s7:elementID` ある場合、そのノードのテキスト値を操作できます。

## 例 {#section-f574fd66dedd4a219aa537d7bdabea23}

ノードに対し `s7:elementID="paragraph1"` て属性が定義されてい `TextGraphic` る場合、次の値が有効であるとします。

`&setVal.paragraph=Hello`

次の例では、段落ノードのテキスト値を「Hello」に設定します。
