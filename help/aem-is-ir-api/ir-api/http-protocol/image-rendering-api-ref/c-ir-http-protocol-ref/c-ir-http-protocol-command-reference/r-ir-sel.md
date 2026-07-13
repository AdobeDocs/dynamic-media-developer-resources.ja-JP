---
title: sel
description: ピクセル位置でオブジェクトを選択します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
TQID: 'https://experienceleague.adobe.com/nmXZZFxdpxJTY4j12JRyhCe-sOZIjajFSfzmPId9X3g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 1%

---

# sel{#sel}

ピクセル位置でオブジェクトを選択します。

` sel= *`x`*, *`y`*[, *` レベル `*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>位置座標をピクセル単位で選択します（int、int）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> レベル </span> </p> </td> 
  <td class="stentry"> <p>グループレベル（int）: </p> </td> 
 </tr> 
</table>

*`x, y`*&#x200B;で指定されたピクセル座標のグループまたはオブジェクトを選択し、新しいMSSを開始します。 選択可能なオブジェクトがピックの場所にない場合、またはピックの場所が無効な場合、`attribute::OnFailSel`で指定されたアクションが実行されます。

*`level`*&#x200B;最も外側のグループを選択するか、ネストされたグループまたはオブジェクトにドリルダウンするかを指定します。 *`level`*&#x200B;が指定されていない場合、最も外側のグループが選択されます。 1に設定すると、最も外側のグループの下の1つのグループレベルが選択されます。 大きな数値（99など）に設定して、最も内側の選択可能なオブジェクトまたはグループを選択します。

## プロパティ {#section-8f27e84d88734a62a5e398e0c9972bdc}

選択コマンド、MSS区切り記号。 オブジェクトの選択は、`obj=`または`sel=`のいずれかで別のオブジェクトが選択されるまで保持されます。

*`x, y`*&#x200B;は、0、0 （画像の左上隅）から&#x200B;*`wid`*-1、*`hei`*-1 （画像の右下隅）の範囲である必要があります。ここで、*`wid`*&#x200B;と&#x200B;*`hei`*&#x200B;は、拡大・縮小されていないビネット ビューのサイズです。

指定した場合、*`level`*&#x200B;は0以上である必要があります。

## 初期設定 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;には該当しません。*`level`* デフォルトは0です。

## 関連項目 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)、[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[属性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)、[属性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)

