---
description: カルーセルビューアのJavaScript APIリファレンス。
seo-description: カルーセルビューアのJavaScript APIリファレンス。
seo-title: 処分する
solution: Experience Manager
title: 処分する
topic: Dynamic media
uuid: 6b4e5bd0-5a32-4e4e-a9a1-c26e8e266aa6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 処分する{#dispose}

カルーセルビューアのJavaScript APIリファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、ビューアによって作成された内部のオブジェクトとコンポーネントを実行時にすべて削除することで、このビューアインスタンスを破棄します。

また、Webページコードは、ビューアインスタンス変数を削除し、Webブラウザーのメモリからビューアを完全に削除する必要があります。

Webページコードが、ビューアが使用するビューアSDKコンポーネント、またはこれらのコンポーネントに格納された外部参照に直接イベントリスナーを登録している場合、そのようなリスナーはWebページコードで明示的に登録解除する必要があり、呼び出す前に削除する必要がありま `dispose()`す。

を呼び出した後は、Viewer APIにアクセスしな `dispose()` いでください。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

