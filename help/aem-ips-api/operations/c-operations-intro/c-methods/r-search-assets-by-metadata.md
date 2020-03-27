---
description: 指定した検索用語のメタデータインデックスリポジトリを検索します。 searchAssetsメソッドなどのアセットデータを返します。
seo-description: 指定した検索用語のメタデータインデックスリポジトリを検索します。 searchAssetsメソッドなどのアセットデータを返します。
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
topic: Scene7 Image Production System API
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# searchAssetsByMetadata{#searchassetsbymetadata}

指定した検索用語のメタデータインデックスリポジトリを検索します。 searchAssetsメソッドなどのアセットデータを返します。

ではユ `searchAssetsByMetadata` ーザ定義のメタデータフィールドを検索できますが、で指定したフィールドは返されませ `responseMetadataArray`ん。 この点を説明するために、次のコード例を示します。

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

この問題を回避するには、検索から返されたア `fieldHandles` セットのうち、を使用して実行する `getAssets` ことがで [きます(getAssetsも参照](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca))。 このメソッドは、対象のアセットのユーザ定義フィールド値を取得します。 次の構文の例を使用して、ユーザ定義メタデータフィールドを検索します。

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## 認証されたユーザータイプ {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>会社の取っ手。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> フィ <span class="varname"> ルタ</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>検索条件の定義に役立つフィルター。 </p> <p>SearchFilterを参照し <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> てください</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> metadataConditionArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>検索条件を定義する条件。 詳しくは、以下を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>応答時にアセットサマリに入力する追加のフィールド。 フィールドは、正規化された形式で指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> recordsPerPage <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>応答が返すアセットの数。 デフォルト値は 1000 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>recordsPerPageページサイズに基づいて、返す結果のページを <span class="codeph"> 指定</span> します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 並べ <span class="varname"> 替え</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>選択したアセットフィールドで並べ替えます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 並べ替 <span class="varname"> え方向</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>並べ替え方向の選択。 デフォルトは昇順です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(searchAssetsByMetadataReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | いいえ | 一致数。 |
| ` *`assetArray`*` | `types:AssetArray` | いいえ | 検索によって返されるアセットの配列。 |

## metadataConditionArrayの詳細 {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

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

`field_handle` は、メタデータ検索キーです。 ドット表記を含めることができます。 次の値を指定できます。

* `asset_id` （接頭辞なし）
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
* `created_at` (次と同じ `modified_at` (フォーム内の日付：7月25日（金）22:13:45 GMT-0500 (CDT)

* `created_by`

**使用可能な演算子**

は、値 [!DNL operator] を比較し、次を含める方法を定義します。

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

は、 `comparison_value` 検索する用語です。

## 例 {#section-53a12b9c023e4e629eddf5719c955ad4}

このコードサンプルでは、次のメタデータ条件を使用して検索を実行します。

* `name` フィールドに次を含め `1000801`ます。

* `dc.rights` フィールドの等 `Per Jessen Schmidt`しい。

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

