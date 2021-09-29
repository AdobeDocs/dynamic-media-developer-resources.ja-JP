---
title: コマンドリファレンス — URL
description: ビデオ 360 ビューアのコマンドリファレンスドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# コマンドリファレンス — URL{#command-reference-url}

ビデオ 360 ビューアのコマンドリファレンスドキュメント。

URL に任意の設定コマンドを設定できます。 または、API メソッド `setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 また、サーバー側の設定レコードで任意の設定属性を指定することもできます。

一部の設定コマンドの先頭に、対応する HTML5 ビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的で、`setContainerId()` API メソッドに渡されるビューアのコンテナの DOM 要素の ID に依存します。 ドキュメントには、そのようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`playback` は次のように記載されています。

```
[Video360Player.|<containerId>_video360Player].playback
```

つまり、このコマンドは次の方法で使用されます。

* `playback` （短い構文）
* `Video360Player.playback` （コンポーネントクラス名で修飾）
* `cont_video360Player.playback` ( コンポーネント ID で修飾、が `cont` コンテナ要素の ID と仮定 )

[ すべてのビューアに共通のコマンドリファレンス — 設定属性 ](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください。
