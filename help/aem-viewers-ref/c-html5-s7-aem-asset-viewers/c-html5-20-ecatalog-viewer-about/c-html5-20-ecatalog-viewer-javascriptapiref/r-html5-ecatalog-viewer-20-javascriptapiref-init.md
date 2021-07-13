---
description: eCatalogビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: init
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

eCatalogビューアのJavaScript APIリファレンス。

`init()`

eCatalogビューアの初期化を開始します。 この時点までに、ビューアのコードがIDで検索できるように、コンテナのDOM要素を作成する必要があります。

コンテナ要素がまだWebページレイアウトの一部ではない場合（例えば、`display:none`スタイルを割り当てて非表示にした場合）、Webページがコンテナ要素をレイアウトに戻す瞬間まで、ビューアは初期化プロセスを中断します。 この場合、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に1回だけ呼び出します。以降の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
