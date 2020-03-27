---
description: PropertySetTypeフィールドとcreatePropertySetTypeParamフィールドの有効な値。
seo-description: PropertySetTypeフィールドとcreatePropertySetTypeParamフィールドの有効な値。
seo-title: PropertySetType
solution: Experience Manager
title: PropertySetType
topic: Scene7 Image Production System API
uuid: 83220180-3272-4552-974d-a73e6aad3483
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PropertySetType{#propertysettype}

PropertySetTypeフィールドとcreatePropertySetTypeParamフィールドの有効な値。

次の値が含まれます。

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 「handle」と入力します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">会社の担当。 <p>注意： 会社のハンドルが存在しない場合、タイプはグローバルです。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 名 <span class="varname"> 前</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 名前を入力します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">プロパティセットのタイプの1つ。 Input (createPropertySetTypeParam<span class="codeph"></span>)を参照してください。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> このタイプのオブジェクトに複数のプロパティセットインスタンスをアタッチできるようにするかどうか。 </td> 
  </tr> 
 </tbody> 
</table>

