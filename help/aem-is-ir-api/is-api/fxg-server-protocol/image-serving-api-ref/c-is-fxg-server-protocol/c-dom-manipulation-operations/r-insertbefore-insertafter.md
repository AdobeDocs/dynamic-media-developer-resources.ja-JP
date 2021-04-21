---
description: ノードの前または後にXMLを設定します。
solution: Experience Manager
title: insertBefore,insertAfter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 3%

---


# insertBefore,insertAfter{#insertbefore-insertafter}

ノードの前または後にXMLを設定します。

`insertBefore=<xml>, insertAfter=<xml>`

FXGノード要素に`s7:elementID`が定義されている場合、このコマンドを使用して、そのノードの前または後にXMLフラグメントを追加できます。

## 例 {#section-1fc8d4135ef94b60b838391e1568e70e}

次のようなGroupタグがある場合：

`<Group visible="true" s7:elementID="inner_shape">`

その後:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

結果：

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

結果：

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
