---
title: init
description: Video360 ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

Video360 ビューアの JavaScript API リファレンス。

`init()`

Video360 ビューアの初期化を開始します。 この時点までに、ビューアのコードが ID で見つけられるように、コンテナの DOM 要素を作成する必要があります。

コンテナ要素がまだ Web ページレイアウトの一部ではない場合（例えば、`display:none` スタイルを割り当てて非表示にした場合）、ビューアは初期化プロセスを中断します。 これは、Web ページでコンテナ要素がレイアウトに戻る時点まで続きます。 このイベントが発生すると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に 1 回だけ呼び出してください。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
