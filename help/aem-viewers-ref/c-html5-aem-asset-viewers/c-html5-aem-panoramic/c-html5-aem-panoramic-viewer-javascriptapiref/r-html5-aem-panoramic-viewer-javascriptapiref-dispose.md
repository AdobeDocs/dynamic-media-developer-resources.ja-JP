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
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
    internal-label: Dynamic Media Classic
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '124'
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
