---
title: printRes
description: 印刷解像度。 応答画像に埋め込まれた印刷解像度の値を上書きします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# printRes{#printres}

印刷解像度。 応答画像に埋め込まれた印刷解像度の値を上書きします。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>印刷解像度（dpi）。 </p></td> 
 </tr> 
</table>

印刷解像度は、通常、カタログエントリの場合は `catalog::PrintResolution` で定義し、それ以外の場合は、ソース画像に埋め込まれた印刷解像度の値で定義します。 テンプレートまたはレイヤー化された複合画像がある場合、応答ファイルに埋め込まれるデフォルトの印刷解像度は、レイヤー番号が最も低いレイヤー画像の印刷解像度です。

印刷解像度を設定しても、返信画像のピクセルサイズは変更されません。

## プロパティ {#section-03c7910ebe234804a319e5d0d8ef3a74}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。

## 初期設定 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
または、ソース画像に埋め込まれた印刷解像度。

## 関連項目 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[カタログ：:PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
