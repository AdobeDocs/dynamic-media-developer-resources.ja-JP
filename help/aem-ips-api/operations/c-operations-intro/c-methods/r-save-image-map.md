---
description: 新しい画像マップを作成するか、既存のマップを編集します。
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 9%

---

# saveImageMap{#saveimagemap}

新しい画像マップを作成するか、既存のマップを編集します。

構文

## 認証済みユーザータイプ {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび書き込みアクセス権を持っている必要があります。

## パラメータ {#section-64f7f5fd8f954fba9fa30eeee556863a}

**入力 (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col4"> 保存する画像マップを含む会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像マップが属する画像アセットのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 画像マップのハンドル。 NULL の場合は画像マップを作成します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名前 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成または保存された画像マップの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 領域の形状の選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 地域 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 地域を定義するポイントのコンマ区切りリストです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> アクション </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>この <span class="codeph"> href </span> IPS インターフェイスで指定された画像マップに関連付けられた値。 </p> <p>次の手順で <span class="codeph"> href </span> の値を指定する場合は、IPS インターフェイスの画像をクリックし、URL をコピーしてこの要素に貼り付け、IPS URL を適切な URL として書式設定します。 例： <span class="codeph"> &amp; </span> 次に <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像マップのリスト内の順序（Z 軸）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 有効 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**出力 (saveImageMapReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| imageMapHandle | `xsd:string` | はい | 新しい画像マップまたは編集された画像マップのハンドル。 |

## 例 {#section-fdac488b640f427c8aa3d549c5032851}

このコードサンプルは、アセットの新しい画像マップを作成します。 領域の形状文字列定数で決定される形状タイプを使用し、新しい画像マップにハンドルを返します。

**リクエスト**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**応答**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```
