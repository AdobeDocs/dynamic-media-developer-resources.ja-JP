---
title: 廃棄する
description: Spin Viewer用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: c19466a8-9fc5-440c-8bb1-c4528937a522
TQID: 'https://experienceleague.adobe.com/DC1eeiEzKZAJpBSvdBLVt-bJXH9qs8M1oCFENzJsjyQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 2%

---

# 廃棄する{#dispose}

Spin Viewer用JavaScript API リファレンス。

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
