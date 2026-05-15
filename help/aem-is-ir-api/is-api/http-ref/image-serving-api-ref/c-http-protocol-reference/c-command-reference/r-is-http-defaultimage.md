---
title: defaultImage
description: デフォルトの返信画像： 画像が見つからない場合に使用する画像またはカタログ エントリを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
TQID: 'https://experienceleague.adobe.com/48NrVSWIy5golPIibmMEc9FeoE24MtwxfEiYV35k7k4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 1%

---

# defaultImage{#defaultimage}

デフォルトの返信画像： 画像が見つからない場合に使用する画像またはカタログ エントリを指定します。

` defaultImage= *` オブジェクト `*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オブジェクト </span> </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト： </p> </td> 
 </tr> 
</table>

*`object`*&#x200B;は、カタログエントリ（テンプレートを含む）または単純な画像ファイルパスのいずれかです。 欠落している画像をデフォルトの画像で置き換えるのに便利です。 この値は、対応するカタログ `attribute::DefaultImage`の値を上書きします。 空の値（`defaultImage=`）を指定すると、デフォルトの画像処理が無効になります。

>[!NOTE]
>
>デフォルトのイメージメカニズムは、SVG オブジェクトには適用されません。 リクエストで指定されたSVG オブジェクトが見つからない場合は、エラーが返されます。

マルチイメージコンポジション内の画像が1つしかない場合でも、`attribute::DefaultImageMode=0`が元のリクエスト全体を置き換える場合、*`object`*&#x200B;が置き換えます。 元のリクエストから保持されるコマンドは`wid=`、`hei=`、`fmt=`、`qlt=`のみです。

`attribute::DefaultImageMode=1`の場合、オブジェクトは見つからないレイヤー画像のみを置き換えます。見つからないレイヤーの属性が適用され、合成が処理され、通常どおり返されます。

## プロパティ {#section-d30923d8dc4042eba10989212dd70887}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。 `req=`が`img`または`tmb`以外の場合、無視されます。

## 制限 {#section-30df31bc8cac41cd917f1e45196779c2}

外部の画像ソースは、デフォルトの画像メカニズムではカバーされません。外部の画像ソースが無効な場合は、エラーが返されます。

ネストされた画像レンダリングまたはFXG レンダリング要求が失敗すると、画像サービングが`DefaultImageMode=0`に戻ります。

## 初期設定 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 関連項目 {#section-745392143c3747a2955e1ae561f58e5f}

[属性：:DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782)、[属性：: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
