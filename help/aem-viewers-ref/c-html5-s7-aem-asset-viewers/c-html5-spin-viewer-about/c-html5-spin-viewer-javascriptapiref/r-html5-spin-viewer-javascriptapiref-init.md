---
title: init
description: スピンビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# init{#init}

スピンビューアの JavaScript API リファレンス。

`init()`

スピンビューアの初期化を開始します。 この時点までにコンテナは `DOM` 要素は、ビューアコードが ID で見つけられるように作成する必要があります。

コンテナ要素がまだ Web ページレイアウトに含まれていない場合 ( 例えば、 `display:none` style — ビューアは初期化プロセスを中断します。 Web ページがコンテナ要素をレイアウトに戻す瞬間まで休止し、その時点でビューアの読み込みが自動的に再開します。

このメソッドは、ビューアのライフサイクルの間に 1 回だけ呼び出します。後続の呼び出しは無視されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
