---
title: defaultImage
description: デフォルトの返信画像。 画像が見つからない場合に使用する画像またはカタログエントリを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---

# defaultImage{#defaultimage}

デフォルトの返信画像。 画像が見つからない場合に使用する画像またはカタログエントリを指定します。

` defaultImage= *` オブジェクト `*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オブジェクト </span> </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト。 </p> </td> 
 </tr> 
</table>

カタログエントリ（テンプレートを含む）または単純な画像ファイルパスを *`object`* 用できます。 不足している画像をデフォルトの画像に置き換える場合に役立ちます。 この値は、対応するカタログ `attribute::DefaultImage` の値をオーバーライドします。 値が空（`defaultImage=`）の場合、デフォルトの画像処理が無効になります。

>[!NOTE]
>
>デフォルトの画像メカニズムは、SVGオブジェクトには適用されません。 リクエストで指定されたSVGオブジェクトが見つからない場合は、エラーが返されます。

`attribute::DefaultImageMode=0` の場合は、複数画像構成で 1 つの画像のみが欠落している場合でも、元のリクエスト全体が *`object`* に置き換えられます。 元のリクエストから保持されるコマンドは、`wid=`、`hei=`、`fmt=`、`qlt=` のみです。

`attribute::DefaultImageMode=1` の場合、オブジェクトは欠落しているレイヤーイメージのみを置き換えます。欠落しているレイヤーの属性が適用され、合成が通常どおり処理されて返されます。

## プロパティ {#section-d30923d8dc4042eba10989212dd70887}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。 `req=` が `img` または `tmb` 以外の場合、無視されます。

## 制限 {#section-30df31bc8cac41cd917f1e45196779c2}

外部の画像ソースはデフォルトの画像メカニズムでカバーされません。外部の画像ソースが有効でない場合はエラーが返されます。

ネストされた画像レンダリングまたは FXG レンダリングリクエストが失敗すると、画像サービングは `DefaultImageMode=0` に戻ります。

## 初期設定 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage` をクリックします。

## 関連項目 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782)、[attribute:: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
