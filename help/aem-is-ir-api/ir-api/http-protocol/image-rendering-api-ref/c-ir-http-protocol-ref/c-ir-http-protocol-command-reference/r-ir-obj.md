---
description: オブジェクトを名前で選択します。 指定したビネットグループを名前で選択し、新しいMSSを開始します。
seo-description: オブジェクトを名前で選択します。 指定したビネットグループを名前で選択し、新しいMSSを開始します。
seo-title: obj
solution: Experience Manager
title: obj
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# obj{#obj}

オブジェクトを名前で選択します。 指定したビネットグループを名前で選択し、新しいMSSを開始します。

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名 </span> 前 </span> </p> </td> 
  <td class="stentry"> <p>グループ名またはパス/名前。 </p> </td> 
 </tr> 
</table>

サブグループまたは個々のオブジェクトは、完全修飾グループパスを使用して選択できます(つまり、ターゲットグループの名前や、すべての親グループの前に/（スラッシュ）で区切ったオブジェクトを指定します)。

指定した名前を持つグループまたはオブジェクトが見つからない場合、で指定したアクションが実 `attribute::OnObjFail` 行されます。

## プロパティ {#section-9463b36e8ff74c81a70c7c2b58927430}

選択コマンド；MSS区切り文字。 またはを使用して別のオブジェクトを選択するまで、オブジェクトの選択は維持 `obj=` されま `sel=`す。

グループ/オブジェクトのパスと名前では、大文字と小文字が区別されません。

## 初期設定 {#section-0c322850512c4896bb551856a549440e}

レンダリング可能なオブジェクトを含むビネット内の最初のグループは、新しいビネットが開かれると自動的に選択されます。

## 関連項目 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)、 [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
