---
title: setVal
description: s7elementID のテキストノード値を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---

# setVal{#setval}

s7:elementID のテキストノード値を設定します。

`setVal.elementID= *[!DNL value]*`

FXG ノード要素に `s7:elementID` 定義済みの場合、そのノードのテキスト値を操作できます。

## 例 {#section-f574fd66dedd4a219aa537d7bdabea23}

次を想定する： `s7:elementID="paragraph1"` 属性が `TextGraphic` ノードの場合、次の値が有効です。

`&setVal.paragraph=Hello`

次の使用例は、段落ノードのテキスト値を「Hello」に設定します。
