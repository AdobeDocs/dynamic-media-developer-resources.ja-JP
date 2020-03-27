---
description: 生のセット定義文字列を使用して汎用アセットセットを作成し、Image Serverに公開します。
seo-description: 生のセット定義文字列を使用して汎用アセットセットを作成し、Image Serverに公開します。
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createAssetSet{#createassetset}

生のセット定義文字列を使用して汎用アセットセットを作成し、Image Serverに公開します。

構文

## 認証されたユーザータイプ {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-3580b586296e42a5b21426085b1bb72d}

**Input (createAssetSet)**

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
   <td colname="col1"> <span class="codeph"> 会社 <span class="varname"> の取 </span> 扱 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセットセットを含む会社のハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> folderHandle <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 新しいアセットセットを作成するフォルダーのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名 </span> 前 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセット名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> サブ <span class="varname"> タイ </span> プ </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> クライアントがアセットセットタイプに対して作成した一意の識別子。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> セット定義文字列内のパラメータ。 <p>これらは、対象のビューアで指定された形式に解決される必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> thumbAssetHandle <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 新しい画像セットのサムネールとして機能するアセットのハンドル。 指定しなかった場合、IPSはセットが参照する最初の画像アセットを使用しようとします。 </td> 
  </tr> 
 </tbody> 
</table>

**setDefinitionの置換関数**

カタログの参照またはパブリケーション中に解決される行で置換関数を指定できます。 置換文字列の形式は次のとおりで `${<substitution_func>}`す。 使用可能な関数を以下に示します。

>[!NOTE]
>
>パラメータリストのハンドルリテラルは、角括弧で囲む必要がありま `([])`す。 置換文字列の外にあるすべてのテキストは、解決時に一字一句出力文字列にコピーされます。

| **置換関数** | **戻り値** |
|---|---|
| `getFilePath([asset_handle>])` | アセットのマスターファイルパス。 |
| `getCatalogId([<asset_handle>])` | アセットのカタログID。 |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | アセットのメタデータ値。 |
| `getThumbCatalogId([<asset_handle>])` | アセットのカタログID（画像ベースのアセットのみ）。関連付けられたサムアセットのカタログID（他のアセットの場合）。 関連するサムアセットが使用できない場合は、空の文字列を返します。 |

**メディアsetDefinition文字列の例**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

カタログ参照時または公開時に、次のような文字列に解決されます。

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**出力(createAssetSet)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | はい | アセットセットのハンドル。 |

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

