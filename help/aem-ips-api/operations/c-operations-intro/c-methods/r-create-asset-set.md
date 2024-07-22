---
title: createAssetSet
description: Image Server に公開する生のセット定義文字列を使用して、汎用アセットセットを作成します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 5%

---

# createAssetSet{#createassetset}

Image Server に公開する生のセット定義文字列を使用して、汎用アセットセットを作成します。

構文

## 許可されているユーザータイプ {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-3580b586296e42a5b21426085b1bb72d}

**入力（createAssetSet）**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 資産セットを含む会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 新しいアセットセットが作成されたフォルダーへのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> の名前 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセット名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセットセットタイプ用にクライアントで作成された一意の ID。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> セット定義文字列のパラメーター。 <p>これらのパラメーターは、ターゲットビューアで指定される形式に解決される必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 新しい画像セットのサムネールとして機能するアセットのハンドル。 指定しない場合、IPS はセットによって参照される最初の画像アセットを使用しようとします。 </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition の置換関数**

カタログ検索または公開時に解決される置換関数をインラインで指定できます。 置換文字列の形式は `${<substitution_func>}` です。 使用可能な関数の概要を以下に示します。

>[!NOTE]
>
>パラメーターリストのハンドル リテラルは、角かっこ `([])` で囲む必要があります。 置換文字列以外のテキストはすべて、解決中に出力文字列にそのままコピーされます。

| **置換関数** | **戻り値** |
|---|---|
| `getFilePath([asset_handle>])` | アセットのプライマリソースファイルパス。 |
| `getCatalogId([<asset_handle>])` | アセットのカタログ ID。 |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | アセットのメタデータ値。 |
| `getThumbCatalogId([<asset_handle>])` | アセットのカタログ ID （画像ベースのアセットのみ）。 関連付けられたサムアセットのカタログ ID （他のアセット用）。 関連するサムアセットが使用できない場合、この関数は空の文字列を返します。 |

**サンプルの Media setDefinition 文字列**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

カタログ参照または公開時に、このプロセスは次のような文字列に解決されます。

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**出力（createAssetSet）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | アセットセットのハンドル。 |

## 例 {#section-fed53089de824d67ab96cd9103d384b4}

**リクエスト**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**応答**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```
