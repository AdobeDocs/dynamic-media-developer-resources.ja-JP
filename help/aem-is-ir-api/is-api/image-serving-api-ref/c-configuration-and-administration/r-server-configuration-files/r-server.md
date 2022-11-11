---
description: プラットフォームサーバー設定が含まれます。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# server.xml{#server-xml}

プラットフォームサーバー設定が含まれます。

この XML ファイルを変更する場合は、有効な XML 構文を維持するように注意する必要があります。それ以外の場合は、 [!DNL Platform Server] を開始できない可能性があります。

変更を有効にするには、 [!DNL Platform Server] このファイルを編集した後、を再起動する必要があります。

次の図は、このファイルで変更できる設定を示しています。 これらの設定の説明については、このドキュメントの前の対応する節を参照してください。 この図は、 [!DNL server.xml].

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
