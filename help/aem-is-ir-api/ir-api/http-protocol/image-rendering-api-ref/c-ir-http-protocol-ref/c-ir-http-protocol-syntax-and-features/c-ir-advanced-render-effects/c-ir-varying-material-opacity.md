---
title: マテリアルの不透明度の変化
description: 不透明度の可変は、重なり合うオブジェクトに適用される単色および繰り返し可能なテクスチャだけでなく、デカールや窓を覆うマテリアルにも対応しています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# マテリアルの不透明度の変化{#varying-material-opacity}

不透明度の可変は、重なり合うオブジェクトに適用される単色および繰り返し可能なテクスチャだけでなく、デカールや窓を覆うマテリアルにも対応しています。

不透明度の情報は、アルファチャンネルを含むRGB画像を使用するだけで提供できます。 さらに、全体的な不透明度は、`opacity=` コマンドを使用して変更できます（RGBとRGBAの両方の画像）。

壁の境界もRGBA画像をサポートしています。主にダイカットの境界をサポートします。

ウィンドウ カバレッジを定義する[!DNL vnw] ファイルには、不透明度チャネルを含めることができます。 レンダラーと繰り返し可能なテクスチャのアルファチャンネルと`opacity=`値を組み合わせることで、薄暗いウィンドウ処理や半透明のウィンドウ処理に幅広い不透明度エフェクトを提供します。

