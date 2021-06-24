---
description: オブジェクト選択エラー処理。 ビネットオブジェクト階層で指定されたパスが一致しないためにobj=コマンドが失敗した場合に実行するアクションを指定します。
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 13%

---

# OnFailObj{#onfailobj}

オブジェクト選択エラー処理。 ビネットオブジェクト階層で指定されたパスが一致しないためにobj=コマンドが失敗した場合に実行するアクションを指定します。

## プロパティ {#section-2c779d9c133a443d9f0aed9fde7b703c}

列挙

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph">デフォルト：:OnFailObj </span>から継承。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>以前の選択内容を維持. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>選択を解除；マテリアルの適用や、オブジェクトの表示/非表示の試みは無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>エラーを返す. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>デフォルトのグループ（ビネット階層の中で、レンダリング可能なオブジェクトを含む最初のグループ）を選択します。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-a5a95a2b4a204a4eae350e5b544d1513}

定義されていない場合は`default::OnFailObj`から継承されます。

## 関連項目 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
