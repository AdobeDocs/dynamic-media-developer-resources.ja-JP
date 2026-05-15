---
title: OnFailObj
description: オブジェクト選択エラー処理。 指定したパスが周辺光量補正オブジェクト階層で一致しないため、obj= コマンドが失敗した場合に実行するアクションを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
TQID: 'https://experienceleague.adobe.com/fHutIGRe9bnq6VfuVdggXDJU6Z3uMeGtDgukP6pdSDw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 7%

---

# OnFailObj{#onfailobj}

オブジェクト選択エラー処理。 指定したパスが周辺光量補正オブジェクト階層で一致しないため、obj= コマンドが失敗した場合に実行するアクションを指定します。

## プロパティ {#section-2c779d9c133a443d9f0aed9fde7b703c}

列挙：

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph">から継承します。デフォルト：:OnFailObj </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>前の選択範囲を維持します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>選択を解除します。マテリアルの適用やオブジェクトの表示/非表示の試みは無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>エラーを返します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>デフォルトグループ（レンダリング可能なオブジェクトを含む周辺光量補正の階層の最初のグループ）を選択します。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-a5a95a2b4a204a4eae350e5b544d1513}

定義されていない場合、`default::OnFailObj`から継承されます。

## 関連項目 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)、[属性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
