---
description: 画像サービング制御スクリプト このスクリプトを使用して、Image Serving Serverスーパーバイザの開始、停止または再起動を行います。これにより、開始、停止または再起動が行われ、他のすべての画像サービングコンポーネントが再起動されます。
seo-description: 画像サービング制御スクリプト このスクリプトを使用して、Image Serving Serverスーパーバイザの開始、停止または再起動を行います。これにより、開始、停止または再起動が行われ、他のすべての画像サービングコンポーネントが再起動されます。
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Scene7 Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# ImageServing{#imageserving}

画像サービング制御スクリプト このスクリプトを使用して、Image Serving Serverスーパーバイザの開始、停止または再起動を行います。これにより、開始、停止または再起動が行われ、他のすべての画像サービングコンポーネントが再起動されます。

## 使用方法 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## コマンド{#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コマンド </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 開始 </span> </p> </td> 
   <td colname="col2"> <p> サーバスーパバイザとその他すべての画像サービングコンポーネントを開始します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> サーバスーパーバイザを含むすべての画像サービングコンポーネントを停止します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 再起動 </span> </p> </td> 
   <td colname="col2"> <p>サーバスーパーバイザを含むすべての画像サービングコンポーネントを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restart { ps | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Tomcat/Platform Server、Image Server、またはSVGを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ステータス[ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Image Server、Tomcat/Platform Server、SVGserverの稼働時間と現在のメモリ使用量、または指定したサーバーのステータスを返します。サーバスーパーバイザが実行されていない場合は、代わりに情報メッセージが返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

