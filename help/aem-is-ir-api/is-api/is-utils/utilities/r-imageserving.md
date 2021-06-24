---
description: 画像サービング制御スクリプト このスクリプトは、Image Serving Serverスーパーバイザを起動、停止または再起動するために使用され、その後、他のすべての画像サービングコンポーネントを起動、停止または再起動します。
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---

# ImageServing{#imageserving}

画像サービング制御スクリプト このスクリプトは、Image Serving Serverスーパーバイザを起動、停止または再起動するために使用され、その後、他のすべての画像サービングコンポーネントを起動、停止または再起動します。

## 使用方法 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## コマンド {#section-90436a0b0f70435f9ac42dafeed2c17b}

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
   <td colname="col2"> <p> サーバスーパーバイザとその他のすべての画像サービングコンポーネントを起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 停止  </span> </p> </td> 
   <td colname="col2"> <p> サーバースーパーバイザを含む、すべての画像サービングコンポーネントを停止します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 再起動 </span> </p> </td> 
   <td colname="col2"> <p>サーバースーパーバイザを含む、すべての画像サービングコンポーネントを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> { psを再起動する | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Tomcat/Platformサーバー、画像サーバー、またはSVGを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ステータス[ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Image Server、Tomcat/Platform Server、SVGserverの稼動時間と現在のメモリ使用量の情報、または指定したサーバーの状態を返します。サーバスーパーバイザが実行されていない場合は、代わりに情報メッセージが返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
