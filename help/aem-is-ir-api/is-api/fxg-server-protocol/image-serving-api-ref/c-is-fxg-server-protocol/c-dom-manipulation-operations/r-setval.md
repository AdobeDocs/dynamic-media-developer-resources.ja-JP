---
description: s7 elementIDのテキストノード値を設定します。
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---

# setVal{#setval}

s7:elementIDのテキストノード値を設定します。

`setVal.elementID= *[!DNL value]*`

FXGノード要素に`s7:elementID`が定義されている場合は、そのノードのテキスト値を操作できます。

## 例 {#section-f574fd66dedd4a219aa537d7bdabea23}

`s7:elementID="paragraph1"`属性が`TextGraphic`ノードに対して定義され、次の値が有効であるとします。

`&setVal.paragraph=Hello`

次の使用例は、段落ノードのテキスト値を「Hello」に設定します。
