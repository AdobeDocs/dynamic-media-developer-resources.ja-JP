---
title: 処分する
description: スマート切り抜きビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 10144ced-3eb1-424a-b478-976cf1f6e9c5
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 2%

---

# 処分する{#dispose}

スマート切り抜きビデオビューア用のJavaScript API リファレンス。

`dispose()`

このビューアインスタンスを破棄するには、ビューアロジックで使用されているすべてのリソースを解放し、ビューアによって実行時に作成されたすべての内部オブジェクトとコンポーネントを削除します。

Web ページのコードでは、ビューアインスタンス変数も削除して、web ブラウザーのメモリからビューアが完全に削除されるようにしてください。

Web ページコードが、ビューアが使用する Viewer SDK コンポーネントに対して直接イベントリスナーを登録した場合、またはそのようなコンポーネントへの外部参照を保存した場合、リスナーの登録を Web ページコードで明示的に解除する必要があります。 また、このような外部コンポーネント参照は、`dispose()` を呼び出す前に削除する必要があります。

`dispose()` が呼び出された後は、Viewer API にアクセスしないでください。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
