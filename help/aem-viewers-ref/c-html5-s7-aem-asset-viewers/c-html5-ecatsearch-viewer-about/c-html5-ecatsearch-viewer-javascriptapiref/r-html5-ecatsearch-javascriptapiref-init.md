---
description: eCatalogビューアのJavaScript APIリファレンス。
seo-description: eCatalogビューアのJavaScript APIリファレンス。
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# init{#init}

eCatalogビューアのJavaScript APIリファレンス。

[!DNL `init()`]

eCatalogビューアの初期化を開始します。 この時点までに、ビューアのコードがIDでコンテナを見つけられるように、コンテナのDOM要素を作成する必要があります。

コンテナ要素がWebページレイアウトの一部ではない場合（例えば、割り当てられたスタイルを使用して非表示にする場合）、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化処理を中断します。 [!DNL `display:none`] この場合、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に1回だけ呼び出します。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

