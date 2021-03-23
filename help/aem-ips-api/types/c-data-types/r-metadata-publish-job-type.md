---
description: メタデータをメタデータサーバに公開します。
seo-description: メタデータをメタデータサーバに公開します。
seo-title: MetadataPublishJobType
solution: Experience Manager
title: MetadataPublishJobType
uuid: 14cbb67e-56dc-4a25-b871-740be7ea7858
feature: Dynamic Mediaクラシック，SDK/API，メタデータ
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 6%

---


# MetadataPublishJobType{#metadatapublishjobtype}

メタデータをメタデータサーバに公開します。

構文

## パラメータ {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"><span class="codeph"> True</span>に設定すると、<i>すべての</i>データが再度メタデータサーバに発行されます。 <p>注意： データの量によっては、処理に数分から数時間かかる場合があります。 </p><p>新規または変更したメタデータのみを公開する場合は、このパラメータを設定しないでください。 </p></td> 
  </tr> 
 </tbody> 
</table>

