---
description: カルーセルビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: 処分する
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 64e9f83f-e17e-4544-825a-fd458e15fdb5
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# dispose{#dispose}

カルーセルビューアのJavaScript APIリファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、ビューアによって作成されたすべての内部オブジェクトとコンポーネントを実行時に削除して、このビューアインスタンスを破棄します。

また、Webページコードは、ビューアインスタンス変数を削除し、Webブラウザーのメモリからビューアを完全に削除する必要があります。

Webページコードが、ビューアが使用するビューアSDKコンポーネントに直接イベントリスナーを登録している場合、そのようなリスナーはWebページコードで明示的に登録解除する必要があり、`dispose()`を呼び出す前にその外部コンポーネント参照を削除する必要があります。

`dispose()`の呼び出し後は、ビューアのAPIにアクセスしないでください。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
