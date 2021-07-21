---
description: 画像セットに関連付けられているアセットのリストを設定します。
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,Admin
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---

# setImageSetMembers{#setimagesetmembers}

画像セットに関連付けられているアセットのリストを設定します。

この操作では、`ImageSets`と`SpinSets`の`pageReset`パラメーターは無視され、値を強制的にtrueにします。

## 許可されたユーザーの種類 {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、画像セットアセットに対する読み取り/書き込みアクセス権と、各メンバーアセットに対する読み取りアクセス権を持っている必要があります。

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>会社の担当。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像セットハンドル </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像セットに属するアセットメンバーの配列。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(setImageSetMembersReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-7b87219034464aa98524178ccee27738}

このコード・サンプルでは、メンバ配列を使用して画像セットのメンバを設定します。

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
