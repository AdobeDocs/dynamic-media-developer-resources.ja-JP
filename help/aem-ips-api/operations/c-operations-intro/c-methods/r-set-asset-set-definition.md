---
description: 既存のアセットセットのセット定義を更新します。
seo-description: 既存のアセットセットのセット定義を更新します。
seo-title: setAssetSetDefinition
solution: Experience Manager
title: setAssetSetDefinition
topic: Dynamic Media Image Production System API
uuid: 2a2dce5d-7a01-49af-ac8b-33ae0b234ecc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 6%

---


# setAssetSetDefinition{#setassetsetdefinition}

既存のアセットセットのセット定義を更新します。

構文

## 認証済みユーザータイプ{#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**入力(setAssetDefinitionParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | アセットが設定されている会社のハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットセットハンドル |
| `*`setDefinition`*` | `xsd:string` | はい | 定義文字列。 以下を参照。 |

**出力(setAssetSetDefinitionReturn)**

IPS APIは、この操作に対する応答を返しません。

## setDefinitionパラメータ：{#section-f88e066bf5294b4f8c12d5d652a5c94c}について

**setDefinition関数**

`setDefinition`置換関数をインラインで指定します。 これらは、カタログ参照中またはパブリケーション上で解決されます。 置換文字列の形式は`${<substitution_func>}`で、次が含まれます。

>[!NOTE]
>
>パラメーターリスト内のハンドルリテラルは、角括弧`([])`で囲む必要があります。 置換文字列の外側のテキストは、解決時に出力文字列にコピーされます。

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 置換関数 </th> 
   <th colname="col2" class="entry"> アセットの </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> プライマリファイルのパス </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> カタログID </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([  <span class="varname"> asset_handle  </span>],[  <span class="varname"> metadata_field_handle  </span>])  </span> </td> 
   <td colname="col2"> メタデータ値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> カタログID 画像ベースのアセット(画像、調整された表示、レイヤー表示)に適用されます。 <p>その他のアセットの場合、サムアセットのカタログID（存在する場合）を返します。 サムアセットがアセットに関連付けられていない場合は、空の文字列を返します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinitionの例**

次のメディアセット定義文字列：

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

ルックアップ時またはパブリケーション時に次の値に解決されます。

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
