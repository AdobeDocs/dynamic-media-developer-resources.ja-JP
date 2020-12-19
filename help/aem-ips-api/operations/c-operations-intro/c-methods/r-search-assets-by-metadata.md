---
description: 指定した検索用語のメタデータインデックスリポジトリを検索します。 searchAssetsメソッドなど、アセットデータを返します。
seo-description: 指定した検索用語のメタデータインデックスリポジトリを検索します。 searchAssetsメソッドなど、アセットデータを返します。
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
topic: Scene7 Image Production System API
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 7%

---


# searchAssetsByMetadata{#searchassetsbymetadata}

指定した検索用語のメタデータインデックスリポジトリを検索します。 searchAssetsメソッドなど、アセットデータを返します。

`searchAssetsByMetadata`ではユーザ定義のメタデータフィールドに対して検索を実行できますが、`responseMetadataArray`で指定したフィールドは返されません。 この点を理解するために、次のコード例を参照してください。

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

null値を返します。

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

この問題を回避するには、検索から返されたアセットの`fieldHandles`を使用して`getAssets`を実行します（[getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)も参照してください）。 このメソッドは、対象のアセットのユーザ定義フィールド値を取得します。 次の構文の例を使用して、ユーザ定義メタデータフィールドを検索します。

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## 認証済みユーザータイプ{#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**入力(searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>会社へのハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> フィルタ</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>検索条件の定義に役立つフィルター。 </p> <p><a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>検索条件を定義する条件。 詳しくは、以下を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アセットサマリの応答時に入力する追加のフィールド。 フィールドは、正規化された形式で指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>応答が返すアセットの数。 デフォルト値は 1000 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p><span class="codeph"> recordsPerPage</span>ページサイズに基づいて、返す結果のページを指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortBy</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>選択したアセットフィールドで並べ替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>並べ替え方向の選択。 が昇順初期設定です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(searchAssetsByMetadataReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | いいえ | 一致の数。 |
| ` *`assetArray`*` | `types:AssetArray` | いいえ | 検索によって返されるアセットの配列。 |

## metadataConditionArrayの詳細{#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**項目構造**

`metadataConditionArray` の構造は次のとおりです。

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**値**

`field_handle` は、メタデータ検索キーです。ドット表記を含めることができます。 使用できる値は次のとおりです。

* `asset_id` （プレフィックスなし）
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (次と同じ `modified_at` (フォーム内の日付：2014年7月25日（金）22:13:45 GMT-0500(CDT)

* `created_by`

**使用可能な演算子**

[!DNL operator]は値の比較方法と以下を定義します。

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

`comparison_value`は、検索する語です。

## 例 {#section-53a12b9c023e4e629eddf5719c955ad4}

このコードのサンプルでは、次のメタデータ条件を使用して検索を実行します。

* `name` フィールドに次を含 `1000801`む。

* `dc.rights` フィールドに等し `Per Jessen Schmidt`い。

**リクエスト**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**応答**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

