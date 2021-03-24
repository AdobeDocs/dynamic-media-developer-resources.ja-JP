---
description: オブジェクト選択エラーの処理。 obj=コマンドが失敗した場合に、ビネットオブジェクト階層で指定のパスが一致しないことが原因で実行されるアクションを指定します。
solution: Experience Manager
title: OnFailObj
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 13%

---


# OnFailObj{#onfailobj}

オブジェクト選択エラーの処理。 obj=コマンドが失敗した場合に、ビネットオブジェクト階層で指定のパスが一致しないことが原因で実行されるアクションを指定します。

## プロパティ {#section-2c779d9c133a443d9f0aed9fde7b703c}

列挙。

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph">既定：:OnFailObj </span>から継承します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>以前の選択内容を維持. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>選択を解除マテリアルの適用や、オブジェクトの表示/非表示を試みても無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>エラーを返す. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>初期設定のグループ（レンダリング可能なオブジェクトを含むビネット階層の最初のグループ）を選択します。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-a5a95a2b4a204a4eae350e5b544d1513}

定義されていない場合は`default::OnFailObj`から継承されます。

## 関連項目 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
