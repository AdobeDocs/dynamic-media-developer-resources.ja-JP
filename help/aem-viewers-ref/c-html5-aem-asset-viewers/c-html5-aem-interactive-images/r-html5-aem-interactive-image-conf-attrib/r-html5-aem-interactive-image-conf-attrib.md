---
title: コマンドリファレンス — 設定属性
description: インタラクティブ画像ビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

インタラクティブ画像ビューアの設定属性ドキュメント。

設定コマンドは、URL、`setParam()`、`setParams()`、またはその両方の API メソッドを使用して設定できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、`setContainerId()` API メソッドに渡されるビューアのコンテナの DOM 要素の ID に依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomstep` コマンドは次のように記述されています。

`[ZoomView.|<containerId>_zoomView].fmt`

つまり、このコマンドは次のように使用できます。

* `fmt` （短い構文）
* `ZoomView.fmt` （コンポーネントクラス名で修飾）
* `cont_zoomView.fmt` ( コンポーネント ID で修飾、 `cont` はコンテナ要素の ID)

[ すべてのビューアに共通のコマンドリファレンス — 設定属性 ](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。
