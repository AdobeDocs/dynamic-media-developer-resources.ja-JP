---
title: sel
description: ピクセル位置でオブジェクトを選択します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%

---

# sel{#sel}

ピクセル位置でオブジェクトを選択します。

` sel= *`x`*, *`y`*[, *`level`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>位置座標をピクセル単位（整数、整数）で選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> レベル </span> </p> </td> 
  <td class="stentry"> <p>グループレベル（整数）。 </p> </td> 
 </tr> 
</table>

*`x, y`* で指定されたピクセル座標でグループまたはオブジェクトを選択し、新しい MSS を開始します。 選択可能なオブジェクトがピック位置にない場合、またはピック位置が有効でない場合、`attribute::OnFailSel` で指定したアクションが実行されます。

*`level`* 最も外側のグループを選択するか、ネストされたグループまたはオブジェクトにドリルダウンするかを指定します。 *`level`* が指定されていない場合は、最も外側のグループが選択されます。 1 に設定すると、一番外側のグループの下にあるグループ レベルが 1 つ選択されます。 99 などの大きな数値に設定すると、最も内側の選択可能なオブジェクトまたはグループを選択できます。

## プロパティ {#section-8f27e84d88734a62a5e398e0c9972bdc}

選択コマンド。MSS 区切り文字。 オブジェクトの選択は、`obj=` または `sel=` を使用して別のオブジェクトを選択するまで持続します。

*`x, y`* 0, 0 （画像の左上隅） ～ *`wid`*-1, *`hei`*-1 （画像の右下、右隅）の範囲で指定する必要があります。ここで、*`wid`* と *`hei`* は拡大縮小されていないビネットビューのサイズです。

指定する場合、*`level`* は 0 以上である必要があります。

## 初期設定 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`* に対するなし。 *`level`* デフォルトは 0 です。

## 関連項目 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)、[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)、[attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
