---
title: 処分する
description: インタラクティブビデオビューアのJavaScript APIリファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 55418b97-3d18-4c1d-b0e3-aefd71f46616
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 処分する{#dispose}

インタラクティブビデオビューアのJavaScript APIリファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、ビューアによって実行時に作成された内側のオブジェクトとコンポーネントをすべて削除することで、このビューアインスタンスを破棄します。

また、Webページコードで、ビューアのインスタンス変数を削除して、Webブラウザーのメモリからビューアを完全に削除する必要があります。

Webページコードで、ビューアが使用するビューアSDKコンポーネントに直接イベントリスナーが登録されている場合、またはそのようなコンポーネントへの外部参照が保存されている場合は、Webページコードで明示的に登録を解除する必要があります。 また、`dispose()`を呼び出す前に、このような外部コンポーネント参照を削除する必要があります。

`dispose()`の呼び出し後は、ビューアAPIにアクセスしないでください。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
