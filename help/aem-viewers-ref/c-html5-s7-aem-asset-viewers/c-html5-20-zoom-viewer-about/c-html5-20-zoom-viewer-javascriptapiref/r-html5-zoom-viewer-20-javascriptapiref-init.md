---
title: init
description: ビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9e83b773-c059-45c6-a249-ef0ed2799a05
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# init{#init}

ビデオビューアの JavaScript API リファレンス。

`init()`

ビデオビューアの初期化を開始します。 この時点までに、ビューアのコードが ID で検索できるように、コンテナの DOM 要素を作成する必要があります。

コンテナ要素がまだ Web ページレイアウトに含まれていない場合 ( 例えば、 `display:none` スタイル ) の場合、ビューアは初期化プロセスを中断します。 これは、Web ページがコンテナ要素をレイアウトに戻す時点までおこないます。 この処理が行われると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に 1 回だけ呼び出します。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
