---
description: 指定したs7 elementIDの属性を削除します。
seo-description: 指定したs7 elementIDの属性を削除します。
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAttr{#deleteattr}

指定したs7:elementIDの属性を削除します。

`deleteAttr.elementID={attributeName%26attributeName}`

FXGノード要素に定義済みの属性があ `s7:elementID` る場合は、このコマンドを使用してそのノードの属性を削除できます。

## 例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

次の例では、元のFXGノ *[!DNL x]*&#x200B;ードか *[!DNL y]*&#x200B;ら属性、お *[!DNL visible]* よびを削除します。
