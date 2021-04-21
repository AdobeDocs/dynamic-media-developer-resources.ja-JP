---
description: 印刷解像度。 応答画像に埋め込まれた印刷解像度の値を上書きします。
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# printRes{#printres}

印刷解像度。 応答画像に埋め込まれた印刷解像度の値を上書きします。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>印刷解像度(dpi)。 </p></td> 
 </tr> 
</table>

通常、プリント解像度はカタログエントリの場合は`catalog::PrintResolution`で定義され、それ以外の場合はソース画像に埋め込まれたプリント解像度の値で定義されます。 テンプレートまたはレイヤー化された複合画像の場合、応答ファイルに埋め込まれる初期設定のプリント解像度は、最も低いレイヤー番号を持つレイヤー画像のプリント解像度です。

プリント解像度を設定しても、返信画像のピクセルサイズは変更されません。

## プロパティ {#section-03c7910ebe234804a319e5d0d8ef3a74}

要求属性。 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` またはソース画像に埋め込まれたプリント解像度。

## 関連項目 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
