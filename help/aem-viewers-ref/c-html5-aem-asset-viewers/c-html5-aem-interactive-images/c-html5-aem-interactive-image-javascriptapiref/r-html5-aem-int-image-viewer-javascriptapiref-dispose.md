---
description: ビデオ画像ビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: 処分する
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# 処分する{#dispose}

ビデオ画像ビューアのJavaScript APIリファレンス。

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
