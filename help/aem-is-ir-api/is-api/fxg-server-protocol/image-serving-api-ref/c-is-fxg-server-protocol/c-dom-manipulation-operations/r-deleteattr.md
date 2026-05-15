---
description: 特定のs7 エレメント IDの任意の属性を削除します。
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
TQID: 'https://experienceleague.adobe.com/dQN741iV4LtlEeq3R4tAnPcBHK-AHrzD-jv7AQ4a5ls'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 48
ht-degree: 2%

---

# deleteAttr{#deleteattr}

特定のs7:elementIDの任意の属性を削除します。

`deleteAttr.elementID={attributeName%26attributeName}`

FXG ノード要素に`s7:elementID`が定義されている場合、このコマンドを使用してそのノードの属性を削除できます。

## 例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

次の使用例は、元のFXG ノードから属性&#x200B;*[!DNL x]*、*[!DNL y]*&#x200B;および&#x200B;*[!DNL visible]*&#x200B;を削除します。
