---
description: デフォルトの返信画像。 画像が見つからない場合に使用する画像またはカタログエントリを指定します。
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# defaultImage{#defaultimage}

デフォルトの返信画像。 画像が見つからない場合に使用する画像またはカタログエントリを指定します。

` defaultImage= *`オブジェクト`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト。 </p> </td> 
 </tr> 
</table>

*`object`* は、カタログエントリ（テンプレートを含む）または単純な画像ファイルパスです。見つからない画像をデフォルトの画像で置き換えるのに役立ちます。 この値は、対応するカタログ`attribute::DefaultImage`の値より優先されます。 空の値(`defaultImage=`)を指定すると、デフォルトの画像処理が無効になります。

>[!NOTE]
>
>デフォルトの画像メカニズムはSVGオブジェクトには適用されません。 リクエストで指定されたSVGオブジェクトが見つからない場合は、エラーが返されます。

`attribute::DefaultImageMode=0`の場合、マルチ画像合成で1つの画像しか見つからなくても、*`object`*&#x200B;は元のリクエスト全体を置き換えます。 元の要求から保持されるコマンドは次のとおりです。`wid=`、`hei=`、`fmt=`、`qlt=`。

`attribute::DefaultImageMode=1`の場合、見つからないレイヤーイメージのみが置き換えられます。見つからないレイヤの属性が適用され、コンポジットが通常どおり処理されて返されます。

## プロパティ {#section-d30923d8dc4042eba10989212dd70887}

リクエスト属性。 現在の画層設定に関係なく適用されます。 `req=`が`img`または`tmb`以外の場合は無視されます。

## 制限事項 {#section-30df31bc8cac41cd917f1e45196779c2}

外部の画像ソースは、デフォルトの画像メカニズムではカバーされません。外部の画像ソースが有効でない場合は、エラーが返されます。

ネストされた画像レンダリングまたはFXGレンダリング要求が失敗すると、画像サービングが`DefaultImageMode=0`に戻る。

## 初期設定 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage` をクリックします。

## 関連項目 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) 、属 [性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
