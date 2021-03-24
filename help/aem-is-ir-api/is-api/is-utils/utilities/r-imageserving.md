---
description: 画像サービング制御スクリプト このスクリプトを使用して、Image Serving Serverスーパーバイザの開始、停止または再起動を行います。これにより、開始、停止または再起動が行われ、他のすべての画像サービングコンポーネントが再起動されます。
solution: Experience Manager
title: ImageServing
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
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

