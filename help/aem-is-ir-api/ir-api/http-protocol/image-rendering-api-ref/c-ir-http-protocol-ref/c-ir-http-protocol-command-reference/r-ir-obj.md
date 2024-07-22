---
title: obj
description: 名前でオブジェクトを選択します。 指定されたビネット グループを名前で選択し、新しい MSS を開始します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# obj{#obj}

名前でオブジェクトを選択します。 指定されたビネット グループを名前で選択し、新しい MSS を開始します。

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> の名前 </span> </span> </p> </td> 
  <td class="stentry"> <p>グループ名またはパス/名前。 </p> </td> 
 </tr> 
</table>

サブグループまたは個々のオブジェクトは、完全修飾グループパスを使用して選択できます（つまり、すべての親グループが先頭に付くターゲットグループまたはオブジェクトの名前を/ （スラッシュ）で区切って指定します）。

指定した名前のグループ/オブジェクトが見つからない場合は、`attribute::OnObjFail` で指定したアクションが実行されます。

## プロパティ {#section-9463b36e8ff74c81a70c7c2b58927430}

選択コマンド。MSS 区切り文字。 オブジェクトの選択は、`obj=` または `sel=` を使用して別のオブジェクトを選択するまで持続します。

グループ/オブジェクトのパスと名前では、大文字と小文字が区別されません。

## 初期設定 {#section-0c322850512c4896bb551856a549440e}

レンダリング可能なオブジェクトを含むビネットの最初のグループは、新しいビネットを開いたときに自動的に選択されます。

## 関連項目 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
