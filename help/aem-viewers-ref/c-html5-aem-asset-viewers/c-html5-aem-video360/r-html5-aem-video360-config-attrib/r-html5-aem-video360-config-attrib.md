---
description: ビデオ360ビューアの設定属性ドキュメント。
seo-description: ビデオ360ビューアの設定属性ドキュメント。
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic media
uuid: 645bba87-3d84-46e9-97fc-7019c5dd87ca
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

ビデオ360ビューアの設定属性ドキュメント。

設定コマンドはURLで設定することも、APIメソッドを使用するこ `setParam()`とも、APIメソッドを `setParams()`使用することも、両方使用することもできます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、 `setContainerId()` APIメソッドに渡されるビューアのコンテナのDOM要素のIDに依存します。 このようなコマンドのオプションのプレフィックスがドキュメントに含まれています。 例えば、コマンドは `playback` 次のように記載されています。

`[VideoPlayer.|<containerId>_videoPlayer].playback`

つまり、このコマンドは次のように使用できます。

* `playback` （短い構文）
* `VideoPlayer.playback` （コンポーネントのクラス名で修飾）
* `cont_videoPlayer.playback` (コンポーネントIDで修飾、 `cont` はコンテナ要素のIDとする)

すべてのビューアに共 [通のコマンドリファレンス — 設定属性も参照してください。](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
