---
title: init
description: eCatalog ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# init{#init}

eCatalog ビューアの JavaScript API リファレンス。

`init()`

eCatalog ビューアの初期化を開始します。 この時点で、ビューアのコードが ID でコンテナを見つけられるように、コンテナの DOM 要素を作成する必要があります。

コンテナ要素がまだ Web ページレイアウトに含まれていない場合 ( 例えば、 `display:none` スタイルの割り当て — 初期化プロセスを中断します。 これは、Web ページがコンテナ要素をレイアウトに戻す時点までおこないます。 この操作を実行すると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に 1 回だけ呼び出します。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
