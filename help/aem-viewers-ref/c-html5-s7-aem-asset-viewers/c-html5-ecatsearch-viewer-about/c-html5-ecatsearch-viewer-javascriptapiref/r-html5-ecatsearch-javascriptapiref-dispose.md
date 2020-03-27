---
description: eCatalogビューアのJavaScript APIリファレンス。
seo-description: eCatalogビューアのJavaScript APIリファレンス。
seo-title: 処分する
solution: Experience Manager
title: 処分する
topic: Dynamic media
uuid: 791c47e9-daab-4500-9cd0-e56ee6fc830e
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# 処分する{#dispose}

eCatalogビューアのJavaScript APIリファレンス。

[!DNL `dispose()`]

ビューアのロジックで使用されるすべてのリソースを解放し、ビューアによって作成された内部のオブジェクトとコンポーネントを実行時にすべて削除することで、このビューアインスタンスを破棄します。

また、Webページコードは、ビューアインスタンス変数を削除し、Webブラウザーのメモリからビューアを完全に削除する必要があります。

Webページコードが、ビューアが使用するビューアSDKコンポーネント、またはこれらのコンポーネントに格納された外部参照に直接イベントリスナーを登録している場合、そのようなリスナーはWebページコードで明示的に登録解除する必要があり、呼び出す前に削除する必要がありま [!DNL `dispose()`]す。

を呼び出した後は、Viewer APIにアクセスしな [!DNL `dispose()`] いでください。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

