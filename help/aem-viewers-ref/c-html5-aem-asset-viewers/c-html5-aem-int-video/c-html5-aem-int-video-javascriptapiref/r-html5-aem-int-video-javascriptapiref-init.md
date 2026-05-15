---
title: init
description: インタラクティブビデオビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
TQID: 'https://experienceleague.adobe.com/Wl6sRHW7Pv-MZxscPeDcxaAKzP1CqAT4RuWeS2-PCVk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 1%

---

# init{#init}

インタラクティブビデオビューアのJavaScript API リファレンス。

`init()`

インタラクティブビデオビューアの初期化を開始します。 この時点までに、ビューアコードがIDで見つけられるように、コンテナ DOM要素を作成する必要があります。

コンテナ要素がまだweb ページレイアウトの一部ではない場合（例えば、割り当てられた`display:none` スタイルを使用して非表示にできる場合など）、ビューアは初期化プロセスを一時停止します。 web ページがコンテナ要素をレイアウトに戻すまで行われます。 このイベントが発生すると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクル中に1回だけ呼び出します。以降の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
