---
description: 特定の s7 要素 ID の属性を削除します。
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---

# deleteAttr{#deleteattr}

特定の s7:elementID の属性を削除します。

`deleteAttr.elementID={attributeName%26attributeName}`

FXG ノード要素に `s7:elementID` が定義されている場合、そのノードの属性は次のコマンドで削除できます。

## 例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

次の例では、元の FXG ノードから *[!DNL x]*、*[!DNL y]*、および *[!DNL visible]* の属性を削除します。
