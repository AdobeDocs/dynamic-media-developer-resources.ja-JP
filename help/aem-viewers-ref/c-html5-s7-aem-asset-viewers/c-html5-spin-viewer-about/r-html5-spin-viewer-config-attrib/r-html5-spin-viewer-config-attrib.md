---
description: スピンビューアの設定属性ドキュメント。
solution: Experience Manager
title: コマンドリファレンス — 設定属性
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

スピンビューアの設定属性ドキュメント。

設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPIメソッドを使用して設定できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomstep`コマンドは次のように記述されています。

`[SpinView.|<containerId>_spinView].zoomstep`

つまり、このコマンドは次のように使用できます。

* `zoomstep` （短い構文）
* `SpinView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_spinView.zoomstep` (コンポーネントIDで修飾、 `cont` はコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
