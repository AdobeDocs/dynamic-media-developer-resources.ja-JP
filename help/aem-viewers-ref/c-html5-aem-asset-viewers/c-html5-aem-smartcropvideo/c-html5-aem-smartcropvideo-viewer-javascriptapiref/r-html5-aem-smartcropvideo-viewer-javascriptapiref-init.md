---
description: スマート切り抜きビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

スマート切り抜きビデオビューアの JavaScript API リファレンス。

`init()`

スマート切り抜きビデオビューアの初期化を開始します。 この時点までに、ビューアのコードが ID で検索できるように、コンテナの DOM 要素を作成する必要があります。

コンテナ要素がまだ Web ページレイアウトに含まれていない場合 ( 例えば、 `display:none` スタイルを it に割り当てました。ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを中断します。 この場合、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクル中に 1 回だけ呼び出します。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
