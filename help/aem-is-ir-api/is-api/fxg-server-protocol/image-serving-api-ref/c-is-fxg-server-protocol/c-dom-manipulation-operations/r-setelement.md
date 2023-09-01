---
title: setElement
description: XML を s7elementID に設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

XML を s7:elementID に設定します。

`setElement.elementID=<XML>`

FXG ノード要素に `s7:elementID` 定義済み、 `<XML>` の値が子要素として置き換えられます。 The `<XML>` はエンコードする必要があります。

## 例 {#section-f23a998b18994dd3b5d4e1965718db9f}

次を想定する： `s7:elementID="group2"` 属性が `Group` ノードの場合、次の値が有効です。

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

次の使用例は、 `group2`ノードを新しい `TextGraphic` 子ノード。
