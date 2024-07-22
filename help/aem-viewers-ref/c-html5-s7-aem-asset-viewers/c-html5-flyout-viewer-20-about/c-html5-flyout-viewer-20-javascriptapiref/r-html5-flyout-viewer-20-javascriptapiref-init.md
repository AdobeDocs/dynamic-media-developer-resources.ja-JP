---
title: 初期化
description: Flyout ビューアの初期化のためのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 1%

---

# 初期化{#init}

Flyout ビューアのJavaScript API リファレンス。

`init()`

Flyout ビューアの初期化を開始します。 この時点で、ビューアコードが ID で見つけられるように、コンテナ DOM 要素を作成する必要があります。

コンテナ要素がまだ web ページレイアウトの一部でない場合（例えば、割り当てられたスタイルを使用して非表示 `display:none` なっている場合など）、ビューアは初期化プロセスを中断します。 Web ページがコンテナ要素をレイアウトに戻す瞬間までこれを繰り返します。 この場合、ビューアの読み込みは自動的に再開されます。

このメソッドは、ビューアのライフサイクル中に 1 回だけ呼び出す必要があり、結果の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
