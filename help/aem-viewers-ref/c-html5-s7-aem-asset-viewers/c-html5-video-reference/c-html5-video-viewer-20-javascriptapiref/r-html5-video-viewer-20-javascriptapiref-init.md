---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: init
solution: Experience Manager
title: init
uuid: 2ee5bddc-957c-4813-9285-d64b9ac7d590
feature: Dynamic Mediaクラシック，ビューア，SDK/API，ビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---


# init{#init}

ビデオビューアのJavaScript APIリファレンス。

`init()`

ビデオビューアの初期化を開始します。 この時点までに、ビューアコードがIDで見つけられるように、コンテナのDOM要素を作成する必要があります。

例えば、コンテナ要素がまだWebページレイアウトの一部ではない場合、`display:none`スタイルを割り当てて非表示にすると、Webページでコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化プロセスを中断します。 この場合、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に1回だけ呼び出してください。以降の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

