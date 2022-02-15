---
title: 処分する
description: ビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 処分する{#dispose}

ビデオビューアの JavaScript API リファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、実行時にビューアで作成された内側のオブジェクトとコンポーネントをすべて削除して、このビューアインスタンスを破棄します。

また、Web ページコードでビューアのインスタンス変数を削除して、Web ブラウザーのメモリからビューアを完全に削除する必要があります。

Web ページコードで、ビューアが使用する Viewer SDK コンポーネントに直接イベントリスナーが登録されている、またはそのようなコンポーネントへの外部参照が格納されている場合は、Web ページコードでそのようなリスナーの登録を明示的に解除する必要があります。 また、を呼び出す前に、このような外部コンポーネント参照を削除する必要があります `dispose()`.

の後で Viewer API にアクセスしない `dispose()` が呼び出されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
