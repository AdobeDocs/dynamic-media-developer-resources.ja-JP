---
title: init
description: インタラクティブ画像ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 675031ab-21bb-49a5-abbc-eca8d2619e49
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

インタラクティブ画像ビューアの JavaScript API リファレンス。

`init()`

インタラクティブ画像ビューアの初期化を開始します。 この時点までに、ビューアのコードが ID で見つけられるように、コンテナの DOM 要素を作成する必要があります。

コンテナ要素がまだ Web ページレイアウトの一部ではない場合（例えば、割り当てられた `display:none` スタイルで非表示になっている場合）、ビューアは初期化プロセスを中断します。 これは、Web ページでコンテナ要素がレイアウトに戻る時点まで続きます。 この操作がおこなわれると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクルの間に 1 回だけ呼び出してください。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
