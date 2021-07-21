---
description: プラットフォームサーバー設定が含まれます。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# server.xml{#server-xml}

プラットフォームサーバー設定が含まれます。

このXMLファイルを変更する場合は、有効なXML構文を維持するように注意する必要があります。そうしないと、Platform Serverの起動に失敗する場合があります。

変更を有効にするには、このファイルを編集した後でPlatform Serverを再起動する必要があります。

次の図は、このファイルで変更できる設定を示しています。 これらの設定の説明については、このドキュメントの前述の対応する節を参照してください。 この図は[!DNL server.xml]の完全な表現ではありません。

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```
