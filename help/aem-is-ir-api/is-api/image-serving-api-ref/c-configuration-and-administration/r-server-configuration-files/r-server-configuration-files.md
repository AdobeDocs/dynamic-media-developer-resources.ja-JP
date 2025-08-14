---
title: サーバー設定ファイル
description: すべての設定ファイルは install_folder/conf にあり、ほとんどのテキストエディターで編集できます。 変更を有効にするには、サーバーを再起動します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# サーバー設定ファイル{#server-configuration-files}

すべての設定ファイルは `install_folder/conf` 内にあり、ほとんどのテキストエディターで編集できます。 変更を有効にするには、サーバーを再起動します。

>[!NOTE]
>
>ほとんどのサーバー設定ファイルには、このドキュメントでは説明されていない追加のプロパティと値が含まれています。 このようなプロパティは内部サーバーで使用するためのものであり、Dynamic Media テクニカルサポートから指示されない限り変更しないでください。

このドキュメントでは、次の設定ファイルについて説明します。

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 設定ファイル </b> </th> 
   <th class="entry"> <b> 説明 </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath">.xml</span> </p> </td> 
   <td> <p>サーバースーパーバイザの設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat 設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath">.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] 設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>カタログサービスの設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath">.conf</span> </p> </td> 
   <td> <p>サーバー監視の設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath">.xml</span> </p> </td> 
   <td> <p>Image Server の設定 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定ファイルについては、このドキュメントの後半で詳しく説明します。
