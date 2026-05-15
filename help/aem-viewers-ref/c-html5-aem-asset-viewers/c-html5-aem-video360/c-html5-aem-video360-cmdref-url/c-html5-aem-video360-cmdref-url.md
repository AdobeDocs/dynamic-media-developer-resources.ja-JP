---
title: コマンドリファレンス - URL
description: Video360 Viewerのコマンドリファレンスドキュメント
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
TQID: 'https://experienceleague.adobe.com/VlMkSjMbXz7uWUKAgT49iab8P-RfJ4mC3qUE0LuQ2zc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 0%

---

# コマンドリファレンス - URL{#command-reference-url}

Video360 Viewerのコマンドリファレンスドキュメント

URLに任意の設定コマンドを設定できます。 または、API メソッド `setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 また、サーバーサイド設定レコードで任意の設定属性を指定することもできます。

一部の設定コマンドには、対応するHTML5 Viewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、そのようなコマンドのオプションのプレフィックスが含まれています。 例えば、`playback`は次のように文書化されています。

```
[Video360Player.|<containerId>_video360Player].playback
```

つまり、このコマンドは次の方法で使用されます。

* `playback` （短い構文）
* `Video360Player.playback` （コンポーネントクラス名で修飾）
* `cont_video360Player.playback` （`cont`がコンテナ要素のIDであると仮定すると、コンポーネント IDで修飾）

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください
