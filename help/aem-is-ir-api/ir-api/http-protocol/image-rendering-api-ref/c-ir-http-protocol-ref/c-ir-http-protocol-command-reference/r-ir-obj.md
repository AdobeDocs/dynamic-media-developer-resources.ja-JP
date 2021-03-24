---
description: 名前でオブジェクトを選択します。 指定したビネットグループを名前と開始で選択し、新しいMSSを指定します。
solution: Experience Manager
title: obj
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# obj{#obj}

名前でオブジェクトを選択します。 指定したビネットグループを名前と開始で選択し、新しいMSSを指定します。

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>グループ名またはパス/名前。 </p> </td> 
 </tr> 
</table>

サブグループまたは個々のオブジェクトは、完全修飾グループパスを使用して選択できます(つまり、すべての親グループの前に/（スラッシュ）で区切ったターゲットグループまたはオブジェクトの名前を指定します)。

指定された名前を持つグループ/オブジェクトが見つからない場合は、`attribute::OnObjFail`で指定されたアクションが実行されます。

## プロパティ {#section-9463b36e8ff74c81a70c7c2b58927430}

選択コマンド；MSS区切り文字。 `obj=`または`sel=`を使用して別のオブジェクトを選択するまで、オブジェクト選択は維持されます。

グループ/オブジェクトのパスと名前は、大文字と小文字が区別されません。

## 初期設定 {#section-0c322850512c4896bb551856a549440e}

レンダリング可能なオブジェクトを含むビネット内の最初のグループは、新しいビネットが開かれたときに自動的に選択されます。

## 関連項目 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
