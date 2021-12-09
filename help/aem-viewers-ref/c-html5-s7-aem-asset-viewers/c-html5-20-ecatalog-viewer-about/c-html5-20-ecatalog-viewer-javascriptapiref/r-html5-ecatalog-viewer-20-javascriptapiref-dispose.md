---
title: 処分する
description: eCatalog ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 827decd9-1f6c-4ac1-8fcc-acc93cfb859d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 処分する{#dispose}

eCatalog ビューアの JavaScript API リファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、実行時にビューアで作成された内側のオブジェクトとコンポーネントをすべて削除して、このビューアインスタンスを破棄します。

また、Web ページコードでビューアのインスタンス変数を削除して、Web ブラウザーのメモリからビューアを完全に削除する必要があります。

Web ページコードがビューアで使用される Viewer SDK コンポーネントに直接イベントリスナーを登録している場合、またはそのようなコンポーネントへの外部参照を保存している場合は、Web ページコードによって明示的に登録解除する必要があります。 また、呼び出しの前に、このような外部コンポーネント参照を削除する必要があります `dispose()`.

の後で Viewer API にアクセスしない `dispose()` が呼び出されます。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
