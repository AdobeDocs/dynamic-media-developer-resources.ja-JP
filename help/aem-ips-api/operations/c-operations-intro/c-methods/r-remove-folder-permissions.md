---
description: フォルダーの権限を削除します。
seo-description: フォルダーの権限を削除します。
seo-title: removeFolderPermissions
solution: Experience Manager
title: removeFolderPermissions
topic: Scene7 Image Production System API
uuid: cd9f7a42-e314-4ec9-abe2-a27581c7cd23
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 11%

---


# removeFolderPermissions{#removefolderpermissions}

フォルダーの権限を削除します。

構文

## 認証済みユーザータイプ{#section-bfa745624f9b43aaba6c226ac6700fe7}

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
   <td colname="col4"> 権限を削除する会社ーを持つフォルダーへのハンドルです。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> フォルダーへのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p><span class="codeph"> true</span>の場合： 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">権限の削除は、すべてのフォルダー権限操作を通じて伝播されます。 </li> 
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

このコードの例では、フォルダーとそのサブフォルダーから権限を削除します。 親フォルダーからのみ権限を削除する必要がある場合は、`updateChildren`を`false`に設定します。

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
