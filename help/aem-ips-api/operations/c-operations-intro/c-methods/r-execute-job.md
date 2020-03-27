---
description: 特定のジョブを実行します。
seo-description: 特定のジョブを実行します。
seo-title: executeJob
solution: Experience Manager
title: executeJob
topic: Scene7 Image Production System API
uuid: e73223c1-9032-4745-92b6-a5840949a824
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# executeJob{#executejob}

特定のジョブを実行します。

構文

## 認証されたユーザータイプ {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**Input (executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col4"> <p>ジョブが属する会社のハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>実行するジョブのハンドル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(executeJobReturn)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-96f71aa58a954293b9a98ff96d86f232}

このコード例では、IPSで実行するようにスケジュールされたジョブを実行します。

**リクエスト**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**応答**

なし
