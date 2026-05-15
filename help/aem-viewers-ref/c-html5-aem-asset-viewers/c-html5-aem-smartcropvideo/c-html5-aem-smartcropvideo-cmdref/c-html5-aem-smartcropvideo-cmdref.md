---
title: コマンドリファレンス – 設定属性
description: スマート切り抜きビデオビューアの設定属性に関するドキュメント。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
TQID: 'https://experienceleague.adobe.com/fTLIy9C3f-00e-wpBTVbQroziLWBo2YT8ieDrdlrnak'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

スマート切り抜きビデオビューアの設定属性に関するドキュメント。

URLに任意の設定コマンドを設定できます。 または、API メソッド `setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 また、サーバーサイド設定レコードで任意の設定属性を指定することもできます。

一部の設定コマンドには、対応するViewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、そのようなコマンドのオプションのプレフィックスが含まれています。 例えば、`playback`は次のように文書化されています。

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

つまり、このコマンドは次の方法で使用されます。

* `playback` （短い構文）
* `SmartCropVideoPlayer.playback` （コンポーネントクラス名で修飾）
* `cont_videoPlayer.playback` （`cont`がコンテナ要素のIDであると仮定すると、コンポーネント IDで修飾）

すべてのビューアに共通の[&#x200B; コマンド参照 – 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)を参照してください

すべてのビューアに共通の[&#x200B; コマンド参照 – URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください
