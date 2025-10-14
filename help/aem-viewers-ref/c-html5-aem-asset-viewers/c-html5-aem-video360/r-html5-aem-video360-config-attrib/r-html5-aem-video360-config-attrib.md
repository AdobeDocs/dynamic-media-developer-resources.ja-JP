---
title: コマンドリファレンス – 設定属性
description: Video360 ビューアの設定属性に関するドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

Video360 ビューアの設定属性に関するドキュメント。

設定コマンドは、URL で設定することも、`setParam()`、`setParams()`、またはその両方の API メソッドを使用して設定することもできます。 サーバーサイドの設定レコードでは、任意の設定属性も指定できます。

一部の設定コマンドには、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付いているものがあります。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、次 `playback` コマンドはドキュメントに記載されています。

`[VideoPlayer.|<containerId>_videoPlayer].playback`

つまり、次の場所でこのコマンドを使用できます。

* `playback` （短い構文）
* `VideoPlayer.playback` （コンポーネントクラス名で修飾）
* `cont_videoPlayer.playback` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。
