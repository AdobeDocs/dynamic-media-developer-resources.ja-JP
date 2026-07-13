---
title: マテリアルの色付け
description: ほとんどのマテリアルは動的にカラー化できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# マテリアルの色付け{#colorizing-materials}

ほとんどのマテリアルは動的にカラー化できます。

カラーアルゴリズムは単純で、色相の範囲が限られているマテリアル画像に最適です。 マテリアルにカラーを適用するには、レンダラーは単に`bgc=`値を減算し、各ピクセル値に`color=`値を追加します。

`color=`が指定されていない場合、色付けは無効になります。 `bgc=`属性はキャビネット マテリアルでは無視されます。代わりに、[!DNL vnc] ファイルに埋め込まれた基本色の値が使用されます。

