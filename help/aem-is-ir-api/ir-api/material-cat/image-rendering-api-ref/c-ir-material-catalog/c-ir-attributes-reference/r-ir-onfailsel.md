---
title: OnFailSel
description: 選択エラーの処理を選択します。 指定したピクセルの位置が選択可能なオブジェクトのマスク領域内にないため、sel= コマンドが失敗した場合に実行するアクションを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
TQID: 'https://experienceleague.adobe.com/rgp6VEJFX8BCZF76fg-1xzrGTuAm87-9HgGHpkNLmtE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 6%

---

# OnFailSel{#onfailsel}

選択エラーの処理を選択します。 指定したピクセルの場所が選択可能なオブジェクトのマスク領域内にないため、`sel=` コマンドが失敗した場合に実行するアクションを指定します。

## プロパティ {#section-cec491e6c5c744f9bfafaaa9d8774f83}

列挙：

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph">から継承します。デフォルト：:OnFailSel </span>。 </p> </td> 
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

## 初期設定 {#section-c25f458f9f8f4236963a95779529e664}

定義されていない場合、`default::OnFailSel`から継承されます。

## 関連項目 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)、[属性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
