---
description: 基本ズームビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: init
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,Business Practitioner
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

基本ズームビューアのJavaScript APIリファレンス。

`init()`

基本ズームビューアの初期化を開始します。 この時点までに、ビューアのコードがIDで見つけられるように、コンテナのDOM要素を作成する必要があります。

コンテナ要素がまだWebページレイアウトの一部ではない場合（例えば、`display:none`スタイルを割り当てて非表示にした場合）、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化プロセスを中断します。 この場合、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に1回だけ呼び出します。以降の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
