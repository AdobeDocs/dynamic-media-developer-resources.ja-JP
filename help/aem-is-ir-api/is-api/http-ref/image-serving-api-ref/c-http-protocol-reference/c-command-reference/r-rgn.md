---
title: rgn
description: 関心のある地域： 合成画像の長方形の関心領域（ROI）をピクセルで表して指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
TQID: 'https://experienceleague.adobe.com/NJ--WHYqUvttsXg-Gn2-FyVUdZJG9SAduOLaaG80nY8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 2%

---

# rgn{#rgn}

関心のある地域： 合成画像の長方形の関心領域（ROI）をピクセルで表して指定します。

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード </span> </p> </td> 
  <td class="stentry"> <p>コンポジット画像の左上隅からROIの左上隅へのピクセルオフセット（int、int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> サイズ </span> </p></td> 
  <td class="stentry"> <p>ROIのサイズ （ピクセル単位（int、int））。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=`は、画像を切り抜かずにROIのみを定義します。 サイズより大きい`wid=`および/または`hei=`も適用すると、合成画像からの追加データが最終返信画像に表示される場合があります。

## プロパティ {#section-53edb35f4e364d7ca13fd0886e8b0c86}

ビュー属性。 現在のレイヤー設定に関係なく適用されます。

合成画像の外側に広がるROIの領域には、`bgc=`がパディングされます。

`rgn=`は、`scl=`、`wid=`、`hei=`、`fit=`、`rect=`、または`align=`を使用して最終的な拡大・縮小とフィッティングの前に適用されます。

## 初期設定 {#section-6a3df8f670084def900ffef9dab7e94a}

合成画像全体（`rgn=0,0,width,height`）。

## 関連項目 {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)、[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
