---
description: 選択エラー処理を選択します。 指定したピクセル位置が選択可能なオブジェクトのマスク領域内にないためにsel=コマンドが失敗した場合に実行するアクションを指定します。
solution: Experience Manager
title: OnFailSel
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 12%

---

# OnFailSel{#onfailsel}

選択エラー処理を選択します。 指定したピクセル位置が選択可能なオブジェクトのマスク領域内にないためにsel=コマンドが失敗した場合に実行するアクションを指定します。

## プロパティ {#section-cec491e6c5c744f9bfafaaa9d8774f83}

列挙

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph">デフォルト：:OnFailSel </span>から継承。 </p> </td> 
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

## 初期設定 {#section-c25f458f9f8f4236963a95779529e664}

定義されていない場合は`default::OnFailSel`から継承されます。

## 関連項目 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ,  [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
