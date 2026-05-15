---
title: 廃棄する
description: パノラマビューアのJavaScript API リファレンス。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
autotag-review: '2026-05-13T22:08:54.657Z'
TQID: 'https://experienceleague.adobe.com/LIJyXNIBKd304RTksUCnN-g5vQjWBTvC-VWQNIgeKjo'
product_v2: id: beaff0dd-a904-4c6b-8290-b527cd877d75id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 2%

---

# 廃棄する{#dispose}

パノラマビューアのJavaScript API リファレンス。

`dispose()`

ビューアロジックで使用されるすべてのリソースを解放し、実行時にビューアで作成されたすべての内部オブジェクトとコンポーネントを削除することで、このビューアインスタンスを破棄します。

Web ページコードは、ビューアインスタンス変数も削除して、ビューアをWeb ブラウザーメモリから完全に削除する必要があります。

Web ページコードが、ビューアで使用されるビューア SDK コンポーネントに直接イベントリスナーを登録している場合、またはそのようなコンポーネントへの外部参照を保存している場合、そのようなリスナーはWeb ページコードによって明示的に登録解除する必要があります。 また、このような外部コンポーネント参照は、`dispose()`を呼び出す前に削除する必要があります。

`dispose()`が呼び出された後は、ビューア APIにアクセスしないでください。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
