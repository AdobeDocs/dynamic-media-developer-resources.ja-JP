---
description: アセットを発行する準備ができているかどうかを指定します。
seo-description: アセットを発行する準備ができているかどうかを指定します。
seo-title: setAssetPublishState
solution: Experience Manager
title: setAssetPublishState
topic: Scene7 Image Production System API
uuid: b7d49d77-573c-4e2a-81d3-196c09d62853
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetPublishState{#setassetpublishstate}

アセットを発行する準備ができているかどうかを指定します。

構文

## 認証されたユーザータイプ {#section-11bec77e50b24461bb8c8aacf016eec8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび書き込みアクセス権を持っている必要があります。

## パラメータ {#section-09d2ba001a2a455a9102550272f3eecb}

**入力(setAssetPublishStateParam)**

<table id="table_23CB72BFB8984CDF82D7207E7D82FC43"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 会社の取っ手。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセットハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">使用可能な状態： 
    <ul id="ul_A2614608DF1E4DB6BF8141D33E59D180"> 
     <li id="li_8C90BFEEE2B14A0184F342018C45EE67"><span class="codeph"> MarkedForPublish</span> </li> 
     <li id="li_C4BC12B304DA4763956C3049AF597D06"><span class="codeph"> NotMarkedForPublish</span> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> contextHandleArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

**出力**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-c31ead6d0e594317a12c120509527792}

次のコード例は、を使用してアセットのパブリケーション状態を設定しま `NotMarkedForPublish`す。

**リクエスト**

```java
<setAssetPublishStateParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <publishState>NotMarkedForPublish</publishState>
</setAssetPublishStateParam>
```

**応答**

なし
