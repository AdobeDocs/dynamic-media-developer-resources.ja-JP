---
description: Image Serverに公開する未加工のセット定義文字列を持つ汎用アセットセットを作成します。
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 6%

---

# createAssetSet{#createassetset}

Image Serverに公開する未加工のセット定義文字列を持つ汎用アセットセットを作成します。

構文

## 許可されたユーザーの種類 {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-3580b586296e42a5b21426085b1bb72d}

**入力(createAssetSet)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセットセットを含む会社のハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 新しいアセットセットが作成されるフォルダーへのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセット名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセットセットタイプに対してクライアントが作成した一意の識別子。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> セット定義文字列のパラメーター。 <p>これらは、対象のビューアで指定された形式に解決する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 新しい画像セットのサムネールとして機能するアセットのハンドル。 指定しなかった場合、IPSはセットが参照する最初の画像アセットを使用しようとします。 </td> 
  </tr> 
 </tbody> 
</table>

**setDefinitionの代替関数**

カタログの参照またはパブリッシュ時に解決される行で置換関数を指定できます。 置換文字列の形式は`${<substitution_func>}`です。 使用可能な関数を以下に列挙します。

>[!NOTE]
>
>パラメーターリストのハンドルリテラルは、角括弧`([])`で囲む必要があります。 置換文字列の外にあるすべてのテキストは、解決時に出力文字列に字句でコピーされます。

| **置換関数** | **戻り値** |
|---|---|
| `getFilePath([asset_handle>])` | アセットのプライマリソースファイルパス。 |
| `getCatalogId([<asset_handle>])` | アセットのカタログID。 |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | アセットのメタデータ値。 |
| `getThumbCatalogId([<asset_handle>])` | アセットのカタログID（画像ベースのアセットのみ）。関連付けられたサムアセットのカタログID（他のアセットの場合）。 関連するサムアセットがない場合、この関数は空の文字列を返します。 |

**メディアsetDefinition文字列のサンプル**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

カタログ参照または公開時に、次のような文字列に解決されます。

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**出力(createAssetSet)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | アセットセットのハンドル。 |

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
