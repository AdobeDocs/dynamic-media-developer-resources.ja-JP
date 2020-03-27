---
description: IPSからアセットを返します。
seo-description: IPSからアセットを返します。
seo-title: getAssets
solution: Experience Manager
title: getAssets
topic: Scene7 Image Production System API
uuid: ca06af8c-1753-4dfa-a7e6-1196ea769730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssets{#getassets}

IPSからアセットを返します。

構文

## 認証されたユーザータイプ {#section-4673c1c9f4314160af8b165eb2dd20cc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーがアクセス権を持つアセットのみを返します。

## パラメータ {#section-bb9cf1ab19ea47acbd9ae58646dbe273}

**Input (getAssetParam)**

<table id="table_15CDEFC7F836411C80AA122E3A701C77"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>会社が取り扱う。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessUserHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>特定のユーザーを装う。 管理者のみが使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessGroupHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>グループでフィルタリング. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>リーフレベルのフォルダーとすべてのサブフォルダーを取得するルートフォルダーです。 除外した場合は、会社のルートが使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：StringArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>応答に含まれるフィールドとサブフィールド。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> excludeFieldArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型：StringArray</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>応答から除外されるフィールドとサブフィールド。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Outpub (getAssetsReturn)**

<table id="table_694932BBBD2C4167871380B2CF514BEA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：AssetArray</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>フィルター条件に一致するアセットの配列。 </p> </td> 
  </tr> 
 </tbody> 
</table>


