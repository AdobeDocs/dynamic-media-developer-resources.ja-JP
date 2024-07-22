---
description: 画像サービング制御スクリプト。 このスクリプトは、Image Serving Server Supervisor を起動、停止、または再起動するために使用されます。これにより、他のすべての Image Serving コンポーネントが起動、停止、または再起動されます。
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# ImageServing{#imageserving}

画像サービング制御スクリプト。 このスクリプトは、Image Serving Server Supervisor を起動、停止、または再起動するために使用されます。これにより、他のすべての Image Serving コンポーネントが起動、停止、または再起動されます。

## 使用方法 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *` コマンド `*`

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
   <td colname="col1"> <p> <span class="codeph"> start </span> </p> </td> 
   <td colname="col2"> <p> Server Supervisor と他のすべての画像サービングコンポーネントを起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop </span> </p> </td> 
   <td colname="col2"> <p> サーバースーパーバイザーを含むすべての画像サービングコンポーネントを停止します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restart </span> </p> </td> 
   <td colname="col2"> <p>サーバースーパーバイザーを含む、すべての画像サービングコンポーネントを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 再起動 { ps |が | svg } </span> </p> </td> 
   <td colname="col2"> <p> Tomcat/[!DNL Platform Server]、Image Server またはSVGを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ステータス [ ps |が | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Image Server、Tomcat/[!DNL Platform Server]、SVGserver の稼動時間と現在のメモリ使用量に関する情報、または指定したサーバーのみのステータスを返します。サーバースーパーバイザーが実行されていない場合は、代わりに情報メッセージが返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
