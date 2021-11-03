---
description: スマート切り抜きビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
title: 処分する
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# 処分する{#dispose}

スマート切り抜きビデオビューアの JavaScript API リファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、実行時にビューアで作成された内側のオブジェクトとコンポーネントをすべて削除して、このビューアインスタンスを破棄します。

また、Web ページコードでビューアのインスタンス変数を削除して、Web ブラウザーのメモリからビューアを完全に削除する必要があります。

Web ページコードがビューア SDK コンポーネントに直接イベントリスナーを登録している場合、そのようなコンポーネントへの外部参照は Web ページコードによって明示的に登録解除され、呼び出しの前に外部コンポーネントの参照を削除する必要があります `dispose()`.

この後はビューア API にアクセスしないでください `dispose()` が呼び出されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
