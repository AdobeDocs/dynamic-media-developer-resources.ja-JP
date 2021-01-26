---
description: ピクセルの位置でオブジェクトを選択
seo-description: ピクセルの位置でオブジェクトを選択
seo-title: sel
solution: Experience Manager
title: sel
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# sel{#sel}

ピクセルの位置でオブジェクトを選択

` sel= *``*, *``*[, *`キシレベル`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>位置の座標をピクセル単位で指定します（整数、整数）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> レベル </span> </p> </td> 
  <td class="stentry"> <p>グループレベル（整数）。 </p> </td> 
 </tr> 
</table>

*`x, y`*&#x200B;で指定されたピクセル座標でグループまたはオブジェクトを選択し、新しいMSSを開始します。 選択可能なオブジェクトが選択位置にない場合、または選択位置が有効でない場合は、`attribute::OnFailSel`によって指定されたアクションが実行されます。

*`level`* 最も外側のグループを選択するか、ネストされたグループまたはオブジェクトにドリルダウンするかを指定します。*`level`*&#x200B;を指定しない場合、一番外側のグループが選択されます。 最も外側のグループの下の1つのグループレベルを選択する場合は、1に設定します。 最も内側の選択可能なオブジェクトまたはグループを選択するには、大きい数値（99など）に設定します。

## プロパティ {#section-8f27e84d88734a62a5e398e0c9972bdc}

選択コマンド；MSS区切り文字。 `obj=`または`sel=`を使用して別のオブジェクトを選択するまで、オブジェクト選択は維持されます。

*`x, y`* は、0, 0（画像の左上隅）～  *`wid`*-1,  *`hei`*-1（画像の左下隅、右隅）の範囲にある必要があります。ここで、 *`wid`* とは、拡大/縮小されないビネット表示のサイズ *`hei`* です。

指定する場合、*`level`*&#x200B;は0以上にする必要があります。

## 初期設定 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;にはなし。 *`level`* の初期設定は0です。

## 関連項目 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , wid= [, ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)hei= [, ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)attribute::DefaultPix [](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
