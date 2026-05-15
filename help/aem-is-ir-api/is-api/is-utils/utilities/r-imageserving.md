---
description: 画像サービングコントロールスクリプト。 このスクリプトは、Image Serving Server Supervisorを起動、停止、または再起動するために使用されます。これにより、他のすべてのImage Serving コンポーネントが起動、停止、または再起動されます。
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
TQID: 'https://experienceleague.adobe.com/KyiS-GblbCE-Q4Exrdz8T1W5thFn9cHellB-1-QYZaw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 1%

---

# ImageServing{#imageserving}

画像サービングコントロールスクリプト。 このスクリプトは、Image Serving Server Supervisorを起動、停止、または再起動するために使用されます。これにより、他のすべてのImage Serving コンポーネントが起動、停止、または再起動されます。

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
   <td colname="col1"> <p> <span class="codeph">開始</span> </p> </td> 
   <td colname="col2"> <p> サーバースーパーバイザーと他のすべての画像サービングコンポーネントを起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">分岐点</span> </p> </td> 
   <td colname="col2"> <p> サーバースーパーバイザーを含むすべてのImage Service コンポーネントを停止します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">を再起動</span> </p> </td> 
   <td colname="col2"> <p>サーバースーパーバイザーを含むすべてのImage Serving コンポーネントを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">再起動{ ps | is | svg } </span> </p> </td> 
   <td colname="col2"> <p> Tomcat/[!DNL Platform Server]、Image Server、またはSVGを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ステータス [ ps | is | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Image Server、Tomcat/[!DNL Platform Server]、SVGserverの稼働時間および現在のメモリ使用情報、または指定したサーバーのみのステータスを返します。サーバースーパーバイザーが実行されていない場合は、代わりに情報メッセージが返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
