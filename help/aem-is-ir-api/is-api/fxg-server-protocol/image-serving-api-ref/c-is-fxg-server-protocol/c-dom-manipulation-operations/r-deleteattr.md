---
description: 特定のs7 elementIDの属性を削除します。
seo-description: 特定のs7 elementIDの属性を削除します。
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

特定のs7:elementIDの属性を削除します。

`deleteAttr.elementID={attributeName%26attributeName}`

FXGノード要素に`s7:elementID`が定義されている場合は、このコマンドを使用して、そのノードの属性を削除できます。

## 例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

次の例では、元のFXGノードから&#x200B;*[!DNL x]*、*[!DNL y]*&#x200B;および&#x200B;*[!DNL visible]*&#x200B;属性を削除します。
