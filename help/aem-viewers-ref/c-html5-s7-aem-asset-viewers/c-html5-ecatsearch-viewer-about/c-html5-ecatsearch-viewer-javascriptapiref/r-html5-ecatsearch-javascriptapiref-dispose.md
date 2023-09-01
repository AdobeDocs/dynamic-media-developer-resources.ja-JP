---
title: 処分する
description: eCatalog ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# 処分する{#dispose}

eCatalog ビューアの JavaScript API リファレンス。

[!DNL `dispose()`]

ビューアのロジックで使用されるすべてのリソースを解放し、実行時にビューアで作成された内側のオブジェクトとコンポーネントをすべて削除して、このビューアインスタンスを破棄します。

また、Web ページコードでビューアのインスタンス変数を削除して、Web ブラウザーのメモリからビューアを完全に削除する必要があります。

Web ページコードで、ビューアが使用する Viewer SDK コンポーネントに直接イベントリスナーが登録されている、またはそのようなコンポーネントへの外部参照が保存されている場合は、Web ページコードによって明示的に登録解除する必要があります。 また、呼び出しの前に、このような外部コンポーネント参照を削除する必要があります [!DNL `dispose()`].

の後で Viewer API にアクセスしない [!DNL `dispose()`] が呼び出されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
