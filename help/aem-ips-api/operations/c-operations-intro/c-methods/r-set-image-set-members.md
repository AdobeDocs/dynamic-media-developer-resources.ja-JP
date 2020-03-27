---
description: 画像セットに関連付けられているアセットのリストを設定します。
seo-description: 画像セットに関連付けられているアセットのリストを設定します。
seo-title: setImageSetMembers
solution: Experience Manager
title: setImageSetMembers
topic: Scene7 Image Production System API
uuid: 84a73ff4-e93f-4764-80e8-e15f1fec1aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setImageSetMembers{#setimagesetmembers}

画像セットに関連付けられているアセットのリストを設定します。

この操作では、のパラメ `pageReset` ーターは無 `ImageSets` 視され、 `SpinSets` 値が強制的にtrueに設定されます。

## 認証されたユーザータイプ {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザは、画像セットアセットに対する読み取りおよび書き込みアクセス権と、各メンバアセットに対する読み取りアクセス権を持っている必要があります。

## パラメータ {#section-2f46efcd24c648aeacba738509426e46}

**入力(setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col4"> <p>会社の担当。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像セットハンドル </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像セットに属するアセットメンバの配列。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(setImageSetMembersReturn)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-7b87219034464aa98524178ccee27738}

このコードの例では、メンバ配列を使用して画像セットのメンバを設定します。

**リクエスト**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**応答**

なし
