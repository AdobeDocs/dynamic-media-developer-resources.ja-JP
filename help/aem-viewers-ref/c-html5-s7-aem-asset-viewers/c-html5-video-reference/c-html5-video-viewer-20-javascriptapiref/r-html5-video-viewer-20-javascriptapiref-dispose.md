---
title: 処分する
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# 処分する{#dispose}

ビデオビューア用のJavaScript API リファレンス。

`dispose()`

このビューアインスタンスを破棄するには、ビューアロジックで使用されているすべてのリソースを解放し、ビューアによって実行時に作成されたすべての内部オブジェクトとコンポーネントを削除します。

Web ページのコードでは、ビューアインスタンス変数も削除して、web ブラウザーのメモリからビューアが完全に削除されるようにしてください。

Web ページのコードで、ビューアが使用する Viewer SDK コンポーネントにイベントリスナーを直接登録した場合、またはそのようなコンポーネントへの外部参照を保存した場合は、web ページのコードでリスナーを明示的に登録解除する必要があります。 また、`dispose()` を呼び出す前に、そのような外部コンポーネント参照を削除する必要があります。

`dispose()` が呼び出された後は、Viewer API にアクセスしないでください。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
