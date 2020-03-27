---
description: 背景色. カラー化可能なテクスチャとデカールの減法カラーを指定します。
seo-description: 背景色. カラー化可能なテクスチャとデカールの減法カラーを指定します。
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

背景色. カラー化可能なテクスチャとデカールの減法カラーを指定します。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGBまたはグレーのカラー値。 </p></td> 
 </tr> 
</table>

イメージレンダリングのテクスチャの色付けアルゴリズムは非常に単純で、のコンポーネント値がテクスチャピクセルの値から減算され、 `bgc=` が加算され、最後に結果がとにクリッピングさ `color=` れま `0,0,0``255,255,255`す。

テクスチャの色付けを一般的に使用する場合、の値は、テク `bgc=` スチャイメージ内で最も重要な色または主要な色になる場合があります。 Scene7 Image Authoringは、テクスチャ画像から適切な色の値を抽出する半自動 `bgc=` ツールを提供します。

テクスチャマテリアルがテクスチャ化されていないビネットオブジェクトに適用される場合、 `bgc=` が指定されていない場合は前景色とし `color=` て適用されます。

## プロパティ {#section-b2db6f147d7f443ba9f671de04c2ef19}

マテリアル属性。 べた塗りとキャビネットのマテリアルでは無視されます。

## 初期設定 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` マテリアルがカタログエントリを基にしている場合は、それ以外の場合は `bgc=808080` （中間のグレー）。

## 例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

主要なRGBカラー120,34,193を持つアパレル生地に色を付けます。

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 関連項目 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) 、 [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
