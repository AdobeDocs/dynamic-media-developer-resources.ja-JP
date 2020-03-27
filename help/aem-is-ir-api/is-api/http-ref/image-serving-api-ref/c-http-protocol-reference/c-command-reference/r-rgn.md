---
description: 目標地域。 合成画像の長方形の目標領域(ROI)をピクセル単位で指定します。
seo-description: 目標地域。 合成画像の長方形の目標領域(ROI)をピクセル単位で指定します。
seo-title: rgn
solution: Experience Manager
title: rgn
topic: Scene7 Image Serving - Image Rendering API
uuid: 08657925-c52a-4279-8357-c26ad5c5ef3d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rgn{#rgn}

目標地域。 合成画像の長方形の目標領域(ROI)をピクセル単位で指定します。

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p> </td> 
  <td class="stentry"> <p>合成画像の左上隅からROIの左上端までのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> サイズ</span> </p></td> 
  <td class="stentry"> <p>ROIのサイズ（ピクセル単位、整数）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` は、画像を切り抜かずにROIを定義するだけです。 また、 `wid=` サイズよ `hei=` り大きい及び/又は大きいデータが適用された場合、合成画像からの追加データが最終的な返信画像に表示され得る。

## プロパティ {#section-53edb35f4e364d7ca13fd0886e8b0c86}

属性を表示します。 現在のレイヤー設定に関係なく適用されます。

合成画像の外側に広がるROIの領域はすべてパディングされま `bgc=`す。

`rgn=` は、、、、、またはを使用して最終的な拡大/縮小と `scl=`フィットの `wid=`前に `hei=`適用さ `fit=`れま `rect=``align=`す。

## 初期設定 {#section-6a3df8f670084def900ffef9dab7e94a}

合成画像全体( `rgn=0,0,width,height`)

## 関連項目 {#section-07883760f25c4d17aedbee36b7883891}

[=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , extend=, wid= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)hei= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)hei=, [scl](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)=, [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[align=, align=, fit=, net=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
