---
title: コマンドリファレンス — 設定属性
description: ズームビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

ズームビューアの設定属性ドキュメント。

任意の設定コマンドを URL で設定するか、 `setParam()`または `setParams()`、またはその両方の API メソッド。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例： `zoomstep` コマンドの説明は次のとおりです。

`[ZoomView.|<containerId>_zoomView].zoomstep`

つまり、コマンドを

* `zoomstep` （短い構文）
* `ZoomView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_zoomView.zoomstep` （コンポーネント ID で修飾、仮定） `cont` はコンテナ要素の ID です )

関連トピック [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
