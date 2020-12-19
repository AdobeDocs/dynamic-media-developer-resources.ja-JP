---
description: ビデオ画像ビューアのJavaScript APIリファレンス。
seo-description: ビデオ画像ビューアのJavaScript APIリファレンス。
seo-title: 処分する
solution: Experience Manager
title: 処分する
topic: Dynamic media
uuid: d9698486-8ffd-4b12-844b-e80b929675ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# dispose{#dispose}

ビデオ画像ビューアのJavaScript APIリファレンス。

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

