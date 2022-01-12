---
title: コマンドリファレンス — 設定属性
description: フライアウトビューアの設定属性ドキュメント
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

フライアウトビューアの設定属性ドキュメント

URL に任意の設定コマンドを設定できます。 または、 `setParam()`, `setParams()`、または両方の API メソッド。 また、サーバー側の設定レコードに任意の設定属性を指定することもできます。

一部の設定コマンドの前に、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付きます。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、 `zoomfactor` コマンドの説明は次のとおりです。

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

コマンドは次のように使用します。

* `zoomfactor` （短い構文）
* `FlyoutZoomView.zoomfactor` （コンポーネントクラス名で修飾）
* `cont_flyout.zoomfactor` ( コンポーネント ID で修飾され、 `cont` はコンテナ要素の ID です )

関連トピック [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
