---
title: コマンドリファレンス – 設定属性
description: パノラマビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

パノラマビューアの設定属性ドキュメント。

設定コマンドは、URL で設定することも、`setParam()` や `setParams()` API メソッドを使用して設定することもできます。 サーバーサイド設定レコードでは、任意の config 属性も指定できます。

一部の設定コマンドでは、対応するHTML5 SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、次 `vrrender` コマンドはドキュメントに記載されています。

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

つまり、このコマンドは次のように使用されます。

* `vrrender` （短い構文）
* `PanoramicView.vrrender` （コンポーネントクラス名で修飾）
* `cont_panoramicView.vrrender` （コンポーネント ID で修飾。cont はコンテナ要素の ID と仮定）


[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) を参照してください。

[ すべてのビューアに共通のコマンドリファレンス - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください。
