---
description: フライアウトビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: 処分する
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,Business Practitioner
exl-id: bf38d481-d8cc-400c-9017-bcb3471f2a10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# 処分する{#dispose}

フライアウトビューアのJavaScript APIリファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、ビューアによって実行時に作成された内側のオブジェクトとコンポーネントをすべて削除することで、このビューアインスタンスを破棄します。

また、Webページコードで、ビューアのインスタンス変数を削除して、Webブラウザーのメモリからビューアを完全に削除する必要があります。

Webページコードがビューアで使用するビューアSDKコンポーネントに直接イベントリスナーを登録している場合、そのようなコンポーネントへの外部参照はWebページコードで明示的に登録解除する必要があり、 `dispose()`を呼び出す前に削除する必要があります。

`dispose()`の呼び出し後は、ビューアAPIにアクセスしないでください。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
