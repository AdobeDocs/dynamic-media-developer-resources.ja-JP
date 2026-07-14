---
description: 既存のアセットセットのセット定義を更新します。
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
TQID: 'https://experienceleague.adobe.com/zBcrMhG1gXiWobSgAZs9xv1jSt3q6Ej0gYUQQ4R3aU0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 200
ht-degree: 5%

---

# setAssetSetDefinition{#setassetsetdefinition}

既存のアセットセットのセット定義を更新します。

構文

## 承認済みユーザータイプ {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**入力（setAssetDefinitionParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | アセットセットを持つ会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | アセットセットセットハンドル |
| setDefinition | `xsd:string` | はい | 定義文字列。 以下を参照してください。 |

**Output （setAssetSetDefinitionReturn）**

IPS APIは、この操作に対する応答を返しません。

## setDefinition パラメーター：概要 {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition関数**

`setDefinition`個の置換関数をインラインで指定します。 これらは、カタログの検索中または公開時に解決されます。 置換文字列の形式は`${<substitution_func>}`で、次のものが含まれます。

>[!NOTE]
>
>パラメーターリスト内のハンドルリテラルは、角括弧`([])`で囲む必要があります。 置換文字列の外部のテキストは、解決中に出力文字列にコピーされます。

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 置換関数 </th> 
   <th colname="col2" class="entry"> アセットの </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath （[ <span class="varname"> asset_handle </span>]） </span> </td> 
   <td colname="col2"> プライマリファイルのパス </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd （[ <span class="varname"> asset_handle </span>]） </span> </td> 
   <td colname="col2"> カタログ ID。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData （[ <span class="varname"> asset_handle </span>],[ <span class="varname"> metadata_field_handle </span>]） </span> </td> 
   <td colname="col2"> メタデータの値： </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId （[ <span class="varname"> asset_handle </span>]） </span> </td> 
   <td colname="col2"> カタログ ID。 画像ベースのアセット（画像、調整済み表示、レイヤー表示）に適用されます。 <p>他のアセットの場合は、サムアセットのカタログ ID （存在する場合）を返します。 アセットに関連付けられているサムアセットがない場合、関数は空の文字列を返します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinitionの例**

このメディアセット定義文字列：

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

参照または公開時に次の問題に解決します。

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## 例 {#section-739b42eec3074cafae285ec015a2d088}

**リクエスト**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**応答**

なし

