---
title: sel
description: ピクセルの位置でオブジェクトを選択します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# sel{#sel}

ピクセルの位置でオブジェクトを選択します。

` sel= *`x`*, *`y`*[, *`レベル`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>位置座標をピクセル単位（整数、整数）で指定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> レベル </span> </p> </td> 
  <td class="stentry"> <p>グループレベル（整数）。 </p> </td> 
 </tr> 
</table>

指定したピクセル座標でグループまたはオブジェクトを選択します。 *`x, y`* 新しい MSS を起動します。 選択可能なオブジェクトが選択位置にない場合、または選択位置が有効でない場合は、 `attribute::OnFailSel` が取得されました。

*`level`* 最も外側のグループを選択するか、ネストされたグループまたはオブジェクトにドリルダウンするかを指定します。 If *`level`* が指定されていない場合、最も外側のグループが選択されます。 1 に設定すると、最も外側のグループの下の 1 つのグループレベルが選択されます。 最も内側の選択可能なオブジェクトまたはグループを選択するには、大きな数（99 など）に設定します。

## プロパティ {#section-8f27e84d88734a62a5e398e0c9972bdc}

選択コマンド；MSS 区切り文字。 オブジェクトの選択は、 `obj=` または `sel=`.

*`x, y`* 0 ～ 0（画像の左上隅）の範囲にする必要があります *`wid`*-1, *`hei`*-1（画像の右下隅） *`wid`* および *`hei`* は、拡大・縮小されていないビネット表示のサイズです。

指定した場合、 *`level`* は、0 以上に設定する必要があります。

## 初期設定 {#section-e13c705a3e76468894b4ec190ed8a893}

なし *`x, y`*. *`level`* デフォルトは 0 です。

## 関連項目 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
