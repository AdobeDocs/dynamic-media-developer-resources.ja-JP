---
title: init
description: eCatalog Viewer用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
TQID: 'https://experienceleague.adobe.com/T33OIUSYMKmrpLGhp8Sia-p8RwyKjEnIMP4Dfp-JgF4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 1%

---

# init{#init}

eCatalog Viewer用JavaScript API リファレンス。

`init()`

eCatalog Viewerの初期化を開始します。 この時点までに、ビューアコードがIDで見つけられるように、コンテナ DOM要素を作成する必要があります。

コンテナ要素がまだweb ページレイアウトの一部ではない場合（例えば、割り当てられた`display:none` スタイルを使用して非表示にできる場合など）、ビューアは初期化プロセスを一時停止します。 web ページがコンテナ要素をレイアウトに戻すまで行われます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

ビューアのライフサイクル中に、このメソッドを1回だけ呼び出します。以降の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
