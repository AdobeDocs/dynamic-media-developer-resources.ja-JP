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
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# dispose{#dispose}

eCatalogビューアのJavaScript APIリファレンス。

[!DNL `dispose()`]

ビューアのロジックで使用されるすべてのリソースを解放し、ビューアによって作成されたすべての内部オブジェクトとコンポーネントを実行時に削除して、このビューアインスタンスを破棄します。

また、Webページコードは、ビューアインスタンス変数を削除し、Webブラウザーのメモリからビューアを完全に削除する必要があります。

Webページコードが、ビューアが使用するビューアSDKコンポーネントに直接イベントリスナーを登録している場合、そのようなリスナーはWebページコードで明示的に登録解除する必要があり、[!DNL `dispose()`]を呼び出す前にその外部コンポーネント参照を削除する必要があります。

[!DNL `dispose()`]の呼び出し後は、ビューアのAPIにアクセスしないでください。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

