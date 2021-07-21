---
description: 1つ以上のアセットの公開ステータスをリセットし、次の公開ジョブでアセットが再公開されるようにします。
solution: Experience Manager
title: forceRepublishAssets
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 4c75af38-4791-4f21-8d1b-4855fcdfd4b1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 8%

---

# forceRepublishAssets{#forcerepublishassets}

1つ以上のアセットの公開ステータスをリセットし、次の公開ジョブでアセットが再公開されるようにします。

構文

## 許可されたユーザーの種類 {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**入力(forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>リセットするアセットを含む会社に対して処理します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アセットのファイルを配信サーバーに再公開することを指定します。 デフォルトは<span class="codeph"> true</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アセットを提供するために使用されるカタログメタデータが、現在のアセットであることを保証するために同期されることを指定します。 このパラメーターは、同じレコードに対するほぼ同時更新で発生する可能性のある競合状態を解決するために使用されます。 デフォルトは<span class="codeph"> false</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray[がた：HandleArray]</span> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>公開ステータスがリセットされるアセットへのハンドルの配列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>公開状態の更新の配列。 </p> </td> 
  </tr> 
 </tbody> 
</table>
