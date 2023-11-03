---
title: コマンドリファレンス — 設定属性
description: パノラマビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

パノラマビューアの設定属性ドキュメント。

任意の設定コマンドを URL で設定するか、 `setParam()` および/または `setParams()` API メソッド。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するHTML5 SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例： `vrrender` コマンドの説明は次のとおりです。

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

つまり、このコマンドは次の方法で使用されます。

* `vrrender` （短い構文）
* `PanoramicView.vrrender` （コンポーネントのクラス名で修飾）
* `cont_panoramicView.vrrender` （コンポーネント ID で修飾、 cont はコンテナ要素の ID と仮定）


詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
