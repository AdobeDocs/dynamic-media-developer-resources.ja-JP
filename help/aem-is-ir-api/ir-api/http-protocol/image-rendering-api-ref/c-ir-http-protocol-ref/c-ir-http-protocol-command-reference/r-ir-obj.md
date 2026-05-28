---
title: obj
description: 名前でオブジェクトを選択します。 指定したビネットグループを名前で選択し、新しいMSSを開始します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
TQID: 'https://experienceleague.adobe.com/te9iyNajxDfgvHqqThbVUc7tBItxfMtxhOMl2eCLOsk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 3%

---

# obj{#obj}

名前でオブジェクトを選択します。 指定したビネットグループを名前で選択し、新しいMSSを開始します。

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">名</span> </span> </p> </td> 
  <td class="stentry"> <p>グループ名またはパス/名前。 </p> </td> 
 </tr> 
</table>

サブグループまたは個々のオブジェクトは、完全修飾グループパスを使用して選択できます（つまり、ターゲットグループまたはオブジェクトの名前をすべての親グループの前に指定し、/（スラッシュ）で区切ります）。

指定された名前のグループまたはオブジェクトが見つからない場合、`attribute::OnObjFail`で指定されたアクションが実行されます。

## プロパティ {#section-9463b36e8ff74c81a70c7c2b58927430}

選択コマンド、MSS区切り記号。 オブジェクトの選択は、`obj=`または`sel=`のいずれかで別のオブジェクトが選択されるまで保持されます。

グループ/オブジェクトのパスと名前は大文字と小文字を区別しません。

## 初期設定 {#section-0c322850512c4896bb551856a549440e}

新しい周辺光量補正を開くと、レンダリング可能なオブジェクトを含む周辺光量補正の最初のグループが自動的に選択されます。

## 関連項目 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [属性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
