---
description: ピクセルの位置でオブジェクトを選択します。
seo-description: ピクセルの位置でオブジェクトを選択します。
seo-title: sel
solution: Experience Manager
title: sel
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sel{#sel}

ピクセルの位置でオブジェクトを選択します。

` sel= *`キシレ`*, *``*[, *`ベル`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>位置の座標をピクセル（整数、整数）で指定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> レベル </span> </p> </td> 
  <td class="stentry"> <p>グループレベル（整数）。 </p> </td> 
 </tr> 
</table>

で指定されたピクセル座標でグループまたはオブジェクトを選 *`x, y`* 択し、新しいMSSを開始します。 選択可能なオブジェクトが選択位置にない場合、または選択位置が無効な場合は、で指定されたアクションが実 `attribute::OnFailSel` 行されます。

*`level`* 最も外側のグループを選択するか、ネストされたグループまたはオブジェクトにドリルダウンするかを指定します。 を指定し *`level`* ない場合、一番外側のグループが選択されます。 1に設定すると、最も外側のグループの下の1つのグループレベルが選択されます。 最も内側の選択可能なオブジェクトまたはグループを選択するには、大きい数（99など）に設定します。

## プロパティ {#section-8f27e84d88734a62a5e398e0c9972bdc}

選択コマンド；MSS区切り文字。 またはを使用して別のオブジェクトを選択するまで、オブジェクトの選択は維持 `obj=` されま `sel=`す。

*`x, y`* は、0, 0（画像の左上隅）～ *`wid`*-1, *`hei`*-1（画像の左下隅、右隅）の範囲で指定する必要があります。ここで、とは、拡大されていないビネットビューのサ *`wid`**`hei`* イズです。

指定する場合は、0 *`level`* 以上の値を指定する必要があります。

## 初期設定 {#section-e13c705a3e76468894b4ec190ed8a893}

なし *`x, y`*。 *`level`* のデフォルト値は0です。

## 関連項目 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::Pix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [default, attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
