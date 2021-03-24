---
description: 選択エラーの処理を選択します。 選択可能なオブジェクトのマスク領域内に指定のピクセル位置がないことが原因でsel=コマンドが失敗した場合に実行するアクションを指定します。
solution: Experience Manager
title: OnFailSel
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 12%

---


# OnFailSel{#onfailsel}

選択エラーの処理を選択します。 選択可能なオブジェクトのマスク領域内に指定のピクセル位置がないことが原因でsel=コマンドが失敗した場合に実行するアクションを指定します。

## プロパティ {#section-cec491e6c5c744f9bfafaaa9d8774f83}

列挙。

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph">既定：:OnFailSel </span>から継承します。 </p> </td> 
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

## 初期設定 {#section-c25f458f9f8f4236963a95779529e664}

定義されていない場合は`default::OnFailSel`から継承されます。

## 関連項目 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ,  [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
