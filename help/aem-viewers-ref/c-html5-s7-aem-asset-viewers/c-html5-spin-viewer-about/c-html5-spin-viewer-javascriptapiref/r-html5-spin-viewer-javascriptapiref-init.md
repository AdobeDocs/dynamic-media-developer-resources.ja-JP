---
description: スピンビューアのJavaScript APIリファレンス。
seo-description: スピンビューアのJavaScript APIリファレンス。
seo-title: init
solution: Experience Manager
title: init
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
feature: Dynamic Mediaクラシック，ビューア，SDK/API，スピンセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---


# init{#init}

スピンビューアのJavaScript APIリファレンス。

`init()`

スピンビューアの初期化を開始します。 この時点までに、ビューアコードがIDで見つけられるように、コンテナ`DOM`要素を作成する必要があります。

コンテナ要素がまだWebページレイアウトの一部ではない場合（例えば、`display:none`スタイルを割り当てて非表示にする場合）、Webページでコンテナ要素がレイアウトに戻る瞬間まで、ビューアは初期化処理を中断します。 この場合、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に1回だけ呼び出してください。以降の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

