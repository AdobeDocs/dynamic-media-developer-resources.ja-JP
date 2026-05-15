---
title: コマンドリファレンス – 設定属性
description: パノラマビューアの設定属性に関するドキュメント。
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2: id: beaff0dd-a904-4c6b-8290-b527cd877d75id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

パノラマビューアの設定属性に関するドキュメント。

任意の設定コマンドは、URLで設定するか、`setParam()`および/または`setParams()` API メソッドを使用して設定できます。 任意のconfig属性をサーバーサイド設定レコードで指定することもできます。

一部の設定コマンドには、対応するHTML5 SDK コンポーネントのクラス名またはインスタンス名が先頭に付いている場合があります。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、そのようなコマンドのオプションのプレフィックスが含まれています。 例えば、`vrrender` コマンドは次のように文書化されています。

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

つまり、このコマンドは次の方法で使用されます。

* `vrrender` （短い構文）
* `PanoramicView.vrrender` （コンポーネントクラス名で修飾）
* `cont_panoramicView.vrrender` （contがコンテナ要素のIDであると仮定して、コンポーネント IDで修飾）


すべてのビューアに共通の[ コマンド参照 – 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)を参照してください

すべてのビューアに共通の[ コマンド参照 – URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください
