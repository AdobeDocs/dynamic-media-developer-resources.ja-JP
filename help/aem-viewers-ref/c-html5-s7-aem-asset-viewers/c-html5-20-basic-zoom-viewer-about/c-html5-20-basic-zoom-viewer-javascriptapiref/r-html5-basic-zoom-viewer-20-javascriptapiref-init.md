---
title: 初期化
description: 基本ズームビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 1%

---

# 初期化{#init}

基本ズームビューアのJavaScript API リファレンス。

`init()`

基本ズームビューアの初期化を開始します。 この時点で、ビューアコードが ID で見つけられるように、コンテナ DOM 要素を作成する必要があります。

コンテナ要素がまだ web ページレイアウトの一部でない場合（例えば、割り当てられたスタイルで非表示 `display:none` なっている場合など）、ビューアは初期化プロセスを中断します。 Web ページがコンテナ要素をレイアウトに戻す瞬間までこれを繰り返します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクル中に 1 回だけ呼び出します。以降の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
