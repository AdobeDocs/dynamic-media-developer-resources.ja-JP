---
description: 画像サービング制御スクリプト。 このスクリプトは、Image Serving Server Supervisor の起動、停止、再起動に使用されます。Image Serving Server Supervisor は、他のすべての画像サービングコンポーネントを起動、停止、または再起動します。
solution: Experience Manager
title: 画像サービング
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# 画像サービング{#imageserving}

画像サービング制御スクリプト。 このスクリプトは、Image Serving Server Supervisor の起動、停止、再起動に使用されます。Image Serving Server Supervisor は、他のすべての画像サービングコンポーネントを起動、停止、または再起動します。

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
   <td colname="col2"> <p> サーバスーパーバイザとその他すべての画像サービングコンポーネントを起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 停止 </span> </p> </td> 
   <td colname="col2"> <p> サーバスーパーバイザを含むすべての画像サービングコンポーネントを停止します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 再起動 </span> </p> </td> 
   <td colname="col2"> <p>サーバースーパーバイザを含め、すべての画像サービングコンポーネントを再起動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> { ps を再起動 | is | svg } </span> </p> </td> 
   <td colname="col2"> <p> Tomcat/を再起動します[!DNL Platform Server]、Image Server、SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ステータス [ ps | is | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Image Server(Tomcat/[!DNL Platform Server]、 、SVGserver、または指定したサーバーのみのステータス。サーバスーパーバイザが実行されていない場合は、代わりに情報メッセージが返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
