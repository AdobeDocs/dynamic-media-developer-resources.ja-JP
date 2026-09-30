---
title: init
description: スマート切り抜きビデオビューアのJavaScript API リファレンス。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e197c4dd-346d-4ef4-beb7-cbd0049dff05
TQID: 'https://experienceleague.adobe.com/8xqHQb7oUGYGZdV1Wd7aQAWsvZR2oNejnLz-KvY7S3o'
product_v2:
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
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 1%
---
# init{#init}

スマート切り抜きビデオビューアのJavaScript API リファレンス。

`init()`

スマート切り抜きビデオビューアの初期化を開始します。 この時点までに、ビューアコードがIDで見つけられるように、コンテナ DOM要素を作成する必要があります。

コンテナ要素がまだweb ページレイアウトの一部ではない場合（例えば、割り当てられた`display:none` スタイルを使用して非表示にできる場合など）、ビューアは初期化プロセスを一時停止します。 web ページがコンテナ要素をレイアウトに戻すまで行われます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

このメソッドは、ビューアのライフサイクル中に1回だけ呼び出します。以降の呼び出しは無視されます。

## パラメーター {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

なし

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアインスタンスへの参照。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
