---
title: init
description: インラインズームビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

インラインズームビューアの JavaScript API リファレンス。

`init()`

ビューアの初期化を開始し、ビューアのコードが ID でビューアを見つけられるようにします。 この時点までにコンテナの DOM 要素を作成する必要があります。

コンテナ要素がまだ Web ページレイアウトに含まれていない場合 ( 例えば、 `display:none` スタイルの割り当て — 初期化プロセスを中断します。 これは、Web ページがコンテナ要素をレイアウトに戻す時点までおこないます。 この操作を行うと、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に 1 回だけ呼び出します。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
