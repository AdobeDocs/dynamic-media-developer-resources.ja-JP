---
title: サーバー設定ファイル
description: すべての設定ファイルはinstall_folder/confにあり、ほとんどのテキストエディターで編集できます。 サーバーを再起動して、変更を有効にします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
TQID: 'https://experienceleague.adobe.com/Gp1W--QzWptazkc1ygnmw59lO8zrNmgmabYMOz8jUG4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 0%

---

# サーバー設定ファイル{#server-configuration-files}

すべての設定ファイルは`install_folder/conf`にあり、ほとんどのテキストエディターで編集できます。 サーバーを再起動して、変更を有効にします。

>[!NOTE]
>
>ほとんどのサーバー設定ファイルには、このドキュメントに記載されていない追加のプロパティと値が含まれています。 これらのプロパティは内部サーバーで使用するためのもので、Dynamic Media テクニカルサポートの指示がない限り変更できません。

このドキュメントでは、次の設定ファイルの設定について説明します。

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>設定ファイル </b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>サーバースーパーバイザー設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] 設定： </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>カタログサービス設定： </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>サーバー監視の設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Image Serverの設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定ファイルについては、このドキュメントの後半で詳しく説明します。
