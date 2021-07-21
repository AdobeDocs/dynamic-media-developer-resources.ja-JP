---
description: 特定のアセットのユーザー定義フィールドの定義。
solution: Experience Manager
title: MetadataField
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: 97175076-9078-4bc4-b3ea-73c3ea772f6a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# MetadataField{#metadatafield}

特定のアセットのユーザー定義フィールドの定義。

`getMetadataFields`操作または`getAssetMetadataField`操作でタグフィールド定義を取得します。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールド名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドタイプ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドのデフォルト値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isRequired</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 必須ステータスを設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isUserDefined</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> メタデータフィールドがユーザーによって定義されているかどうかを判定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">IPSシステム固有のメタデータを非表示または公開します。 <a href="../../operations/c-operations-intro/c-methods/r-get-metadata-fields.md#reference-170337127801401d9ea54bd4ccf28efe" format="dita" scope="local"> getMetadataFields</a>および<a href="../../operations/c-operations-intro/c-methods/r-get-asset-metadata-fields.md#reference-ea57f8e98d3e443da66114550b0d0a28" format="dita" scope="local"> getAssetMetadataFields</a>から返されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>値が設定されたときにメタデータフィールドタイプが適用される（検証される）かどうかを示すbooleanフラグ。 </p> <p>trueに設定すると、<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>に無効な値が設定された場合に、フォルトがスローされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 選択したタグが指す共有列挙値のセットを作成できます。 </td> 
  </tr> 
 </tbody> 
</table>
