---
description: メタデータサーバにメタデータを公開します。
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL MetadataPublishJobType]{#metadatapublishjobtype}

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
   <td colname="col3">に設定 <span class="codeph"> True</span> 公開する <i>すべて</i> データをメタデータサーバに再度送信します。 <p>注意：データの量によっては、この処理に数分から数時間かかる場合があります。 </p><p>新しいメタデータまたは変更したメタデータのみを公開する場合は、このパラメーターを設定しないでください。 </p></td> 
  </tr> 
 </tbody> 
</table>
