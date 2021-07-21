---
description: メタデータサーバにメタデータを公開します。
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---

# MetadataPublishJobType{#metadatapublishjobtype}

メタデータサーバにメタデータを公開します。

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
   <td colname="col3"><span class="codeph"> True</span>に設定すると、<i>すべての</i>データがメタデータサーバに再び公開されます。 <p>注意： データの量によっては、数分から数時間かかる場合があります。 </p><p>新規または変更したメタデータのみを公開する場合は、このパラメーターを設定しないでください。 </p></td> 
  </tr> 
 </tbody> 
</table>
