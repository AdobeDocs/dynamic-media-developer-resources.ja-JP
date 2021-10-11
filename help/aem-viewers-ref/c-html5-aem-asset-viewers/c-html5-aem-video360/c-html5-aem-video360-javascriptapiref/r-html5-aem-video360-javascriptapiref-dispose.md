---
title: 処分する
description: Video360 ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 処分する{#dispose}

Video360 ビューアの JavaScript API リファレンス。

`dispose()`

ビューアのロジックで使用されるすべてのリソースを解放し、ビューアが実行時に作成した内側のオブジェクトとコンポーネントをすべて削除して、このビューアインスタンスを破棄します。

また、Web ページコードでビューアのインスタンス変数を削除して、Web ブラウザーのメモリからビューアを完全に削除する必要があります。

Web ページコードで、ビューアが使用するビューア SDK コンポーネントに直接イベントリスナーが登録されている場合、またはそのようなコンポーネントへの外部参照が格納されている場合は、Web ページコードによって明示的に登録解除する必要があります。 また、`dispose()` を呼び出す前に、このような外部コンポーネント参照を削除する必要があります。

`dispose()` の呼び出し後は、ビューア API にアクセスしないでください。

## パラメータ {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
