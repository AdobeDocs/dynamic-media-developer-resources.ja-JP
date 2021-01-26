---
description: 1つ以上のアセットの公開ステータスをリセットし、次の公開ジョブでアセットが再公開されるようにします。
seo-description: 1つ以上のアセットの公開ステータスをリセットし、次の公開ジョブでアセットが再公開されるようにします。
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
topic: Dynamic Media Image Production System API
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 8%

---


# forceRepublishAssets{#forcerepublishassets}

1つ以上のアセットの公開ステータスをリセットし、次の公開ジョブでアセットが再公開されるようにします。

構文

## 認証済みユーザータイプ{#section-3d5a3e3afea748d69845de5c8c376448}

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
   <td colname="col4"> <p>リセットするアセットを含む会社ーを処理します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アセットのファイルが配信サーバに再公開されることを指定します。 デフォルトは<span class="codeph"> true</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>アセットを提供するために使用されるカタログメタデータが、現在のアセットであることを保証するために同期されることを指定します。 このパラメーターは、同じレコードに対するほぼ同時更新時に発生する可能性のある競合条件を解決するために使用されます。 デフォルトは<span class="codeph"> false</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray</span> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>発行ステータスがリセットされるアセットへのハンドルの配列。 </p> </td> 
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
   <td colname="col2"> <span class="codeph"> 種類：PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パブリッシュ状態の更新の配列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

