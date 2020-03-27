---
description: 特定のアセットのユーザー定義フィールドの定義。
seo-description: 特定のアセットのユーザー定義フィールドの定義。
seo-title: MetadataField
solution: Experience Manager
title: MetadataField
topic: Scene7 Image Production System API
uuid: 6156be6e-efa5-4e90-928d-2ab936668154
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MetadataField{#metadatafield}

特定のアセットのユーザー定義フィールドの定義。

または演算を使用してタグフィールドの定 `getMetadataFields` 義を取得 `getAssetMetadataField` します。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 名 <span class="varname"> 前</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールド名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドの種類。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドのデフォルト値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 必 <span class="varname"> 須</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 必要なステータスを設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isUserDefined</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> メタデータフィールドがユーザーによって定義されているかどうかを判定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> isHidden</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">IPSシステム固有のメタデータを表示または非表示にします。 getMetadataFieldsとgetAssetMetadataFieldsから返 <a href="../../operations/c-operations-intro/c-methods/r-get-metadata-fields.md#reference-170337127801401d9ea54bd4ccf28efe" format="dita" scope="local"> されま</a><a href="../../operations/c-operations-intro/c-methods/r-get-asset-metadata-fields.md#reference-ea57f8e98d3e443da66114550b0d0a28" format="dita" scope="local"></a>す。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>値が設定されたときにメタデータフィールドタイプが適用（検証）されるかどうかを示すbooleanフラグです。 </p> <p>trueに設定した場合、setAssetMetadata <span class="codeph"> /batchSetAssetMetadataに無効な値が設定された場合にエラーが発生し</span> ます<span class="codeph"></span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> initialTagValue <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 選択したタグが参照できる共有列挙値のセットを作成できます。 </td> 
  </tr> 
 </tbody> 
</table>

