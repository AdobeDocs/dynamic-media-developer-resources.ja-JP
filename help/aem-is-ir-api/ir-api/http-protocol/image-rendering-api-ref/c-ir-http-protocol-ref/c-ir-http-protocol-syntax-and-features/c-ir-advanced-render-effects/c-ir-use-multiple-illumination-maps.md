---
title: 複数のイルミネーション マップの使用
description: アプリケーションによっては、異なる種類のマテリアルに対して異なる照明マップが必要な場合があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
TQID: 'https://experienceleague.adobe.com/VVZ1IdVJ85V-mIrdN6O8Vs-gb4PTsnjxyHnC8oEh1y0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# 複数のイルミネーション マップの使用{#using-multiple-illumination-maps}

アプリケーションによっては、異なる種類のマテリアルに対して異なる照明マップが必要な場合があります。

各ビネットに対して最大3つのイルミネーションマップを作成できます。 レンダリング操作のイルミネーション マップは、`illum=`および`gloss=` コマンドで選択されます。

**デフォルトの選択** - `illum=`または`gloss=`が指定されていない場合、レンダラーは最初に作成された照明マップ（通常はマップ A、別名「フラット」照明マップ）を使用します。

**自動選択と`gloss=`** - `illum=`が指定されていないか、`-1`に設定されている場合、レンダラーは指定された`gloss=`値を、周辺光量補正の各照明マップに関連付けられた光沢値と比較します。 光沢値が指定した`gloss=`に最も近い照明マップを選択します。

**`illum=`**&#x200B;を使用した明示的な選択 – `illum=`が指定され、`0`、`1`または`2`に設定されている場合、レンダラーは対応する照明マップを使用します。`gloss=`は照明マップの選択に無視されます。

周辺光量補正に照明マップが1つしか含まれていない場合、レンダラーはそのマップを使用し、`illum=`および`gloss=` コマンドを無視します。

