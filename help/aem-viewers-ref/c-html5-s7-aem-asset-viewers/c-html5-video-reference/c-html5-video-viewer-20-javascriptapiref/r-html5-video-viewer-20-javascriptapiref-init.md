---
title: 初期化
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# 初期化{#init}

ビデオビューア用のJavaScript API リファレンス。

`init()`

ビデオビューアの初期化を開始します。 この時点で、ビューアコードが ID で見つけられるように、コンテナ DOM 要素を作成する必要があります。

コンテナ要素がまだ web ページレイアウトの一部でない場合（例えば、割り当てられたスタイルで非表示になってい `display:none` 場合など）、ビューアは初期化プロセスを中断します。 Web ページがコンテナ要素をレイアウトに戻す瞬間までこれを繰り返します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクル中に 1 回だけ呼び出します。以降の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
