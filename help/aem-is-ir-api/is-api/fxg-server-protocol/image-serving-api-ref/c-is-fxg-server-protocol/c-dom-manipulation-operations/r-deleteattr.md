---
description: 指定したs7 elementIDの属性を削除します。
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# deleteAttr{#deleteattr}

指定したs7:elementIDの属性を削除します。

`deleteAttr.elementID={attributeName%26attributeName}`

FXGノード要素に`s7:elementID`が定義されている場合は、このコマンドを使用してそのノードの属性を削除できます。

## 例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

この例では、元のFXGノードから属性&#x200B;*[!DNL x]*、*[!DNL y]*、および&#x200B;*[!DNL visible]*&#x200B;を削除します。
