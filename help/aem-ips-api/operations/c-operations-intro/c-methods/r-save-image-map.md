---
description: 新しい画像マップを作成するか、既存のマップを編集します。
seo-description: 新しい画像マップを作成するか、既存のマップを編集します。
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
topic: Scene7 Image Production System API
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageMap{#saveimagemap}

新しい画像マップを作成するか、既存のマップを編集します。

構文

## 認証されたユーザータイプ {#section-9ef194a67b3546fb82ed7bb294bc2714}

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

**入力(saveImageMapParam)**

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
   <td colname="col1"> <span class="codeph"> 会社 <span class="varname"> の取 </span> 扱 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 保存する画像マップを持つ会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> asset <span class="varname"> Handle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像マップが属する画像アセットのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageMapHandle <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 画像マップのハンドル。 NULLの場合に画像マップを作成します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名 </span> 前 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成または保存される画像マップの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> シェイ <span class="varname"> プの種 </span> 類 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 領域の形状の選択 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 領 </span> 域 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 領域を定義するポイントのコンマ区切りリストです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 作 </span> 用 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>IPSイン <span class="codeph"> ター </span> フェイスで指定された画像マップに関連付けられたhref値。 </p> <p>href値を取得す <span class="codeph"> るに </span> は、IPSインターフェイスの画像をクリックし、URLをコピーしてこの要素に貼り付け、IPS URLを適切なURLとして形式設定します。 例えば、&amp;は <span class="codeph"> &amp;amp; </span> に <span class="codeph"> なります。 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 位 </span> 置 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像マップ（Z軸）のリスト内の順序。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 有 </span> 効 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**出力(saveImageMapReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | はい | 新しい画像マップまたは編集した画像マップのハンドル。 |

## 例 {#section-fdac488b640f427c8aa3d549c5032851}

このコードサンプルを使用すると、アセットの新しい画像マップを作成できます。 領域の形状文字列定数で決定された形状タイプを使用し、新しい画像マップにハンドルを返します。

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

