---
description: 新しい画像マップを作成するか、既存のマップを編集します。
seo-description: 新しい画像マップを作成するか、既存のマップを編集します。
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 8%

---


# saveImageMap{#saveimagemap}

新しい画像マップを作成するか、既存のマップを編集します。

構文

## 認証済みユーザータイプ{#section-9ef194a67b3546fb82ed7bb294bc2714}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 保存する画像マップを含む会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像マップが属する画像アセットのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 画像マップのハンドル。 NULLの場合に画像マップを作成します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成または保存される画像マップの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 領域の形状の選択 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> region  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 領域を定義するポイントのカンマ区切りリスト。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> action  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>IPSインターフェイスで指定された画像マップに関連付けられている<span class="codeph"> href </span>値。 </p> <p><span class="codeph"> href </span>値を取得するには、IPSインターフェイスの画像をクリックし、URLをコピーしてこの要素に貼り付け、IPS URLを適切なURLに形式設定します。 例えば、<span class="codeph"> &amp; </span>は<span class="codeph"> &amp;amp；になります。</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像マップ（Z軸）のリスト内の順序。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enabled  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**出力(saveImageMapReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | はい | 新しいまたは編集した画像マップのハンドル。 |

## 例 {#section-fdac488b640f427c8aa3d549c5032851}

このコードのサンプルを使用すると、アセット用の新しい画像マップを作成できます。 領域の形状文字列定数によって決まる形状の種類を使用し、新しい画像マップにハンドルを返します。

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

