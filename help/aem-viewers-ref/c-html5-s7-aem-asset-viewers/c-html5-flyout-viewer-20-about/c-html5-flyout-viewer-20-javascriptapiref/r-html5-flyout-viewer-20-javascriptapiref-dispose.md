---
title: 処分する
description: Flyout ビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bf38d481-d8cc-400c-9017-bcb3471f2a10
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# 処分する{#dispose}

Flyout ビューアのJavaScript API リファレンス。

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
