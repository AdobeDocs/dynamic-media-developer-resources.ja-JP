---
description: eCatalogビューアのJavaScript APIリファレンス。
seo-description: eCatalogビューアのJavaScript APIリファレンス。
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 142381e4-aa3c-46dd-a0bd-4e090d0003e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

eCatalogビューアのJavaScript APIリファレンス。

`init()`

eCatalogビューアの初期化を開始します。 この時点までに、ビューアのコードがIDでコンテナを見つけられるように、コンテナのDOM要素を作成する必要があります。

コンテナ要素がWebページレイアウトの一部ではない場合（例えば、割り当てられたスタイルを使用して非表示にする場合）、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を中断します。 `display:none` この場合、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に1回だけ呼び出します。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```

