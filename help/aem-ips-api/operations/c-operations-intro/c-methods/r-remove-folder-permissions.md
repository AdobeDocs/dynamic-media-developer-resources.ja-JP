---
description: フォルダーの権限を削除します。
solution: Experience Manager
title: removeFolderPermissions
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 10830980-d504-4610-96c9-730937453256
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 11%

---

# removeFolderPermissions{#removefolderpermissions}

フォルダーの権限を削除します。

構文

## 許可されたユーザーの種類 {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-7efa68377fd846219b906d354ae64ed3}

**入力(removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 削除する権限を持つフォルダーを持つ会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> フォルダーを処理します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p><span class="codeph"> true</span>の場合： 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">権限の削除は、すべてのフォルダー権限操作を通じて反映されます。 </li> 
     </ul> </p> <p><span class="codeph"> false</span>の場合： 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">この操作は、指定したフォルダーにのみ影響します。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(removeFolderPermissionsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

このコードサンプルを使用すると、フォルダーとそのサブフォルダーから権限を削除できます。 権限を親フォルダーからのみ削除する必要がある場合は、 `updateChildren`を`false`に設定します。

**リクエスト**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**応答**

なし
