---
title: 初期化
description: カルーセルビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 00e09e26-1380-487c-9512-34d805f1330d
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---

# 初期化{#init}

カルーセルビューアのJavaScript API リファレンス。

`init()`

カルーセルビューアの初期化を開始します。 この時点で、ビューアコードが ID で見つけられるように、コンテナ DOM 要素を作成する必要があります。

コンテナ要素がまだ web ページレイアウトの一部でない場合（例えば、スタイルを使用して非表示 `display:none` なっている場合など）、ビューアは初期化プロセスを中断します。 Web ページがコンテナ要素をレイアウトに戻した時点でビューアの読み込みが自動的に再開されるまで停止されます。

このメソッドは、ビューアのライフサイクル中に 1 回だけ呼び出します。以降の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
