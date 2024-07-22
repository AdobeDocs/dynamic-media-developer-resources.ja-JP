---
description: Platform サーバー設定が含まれます。
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

Platform サーバー設定が含まれます。

この XML ファイルを変更する場合、有効な XML 構文を維持するよう注意する必要があります。そうしないと、[!DNL Platform Server] が起動しない場合があります。

変更を有効にするには、このファイルの編集後に [!DNL Platform Server] を再起動する必要があります。

次の図は、このファイルで変更される可能性のある設定を示しています。 これらの設定の説明については、このドキュメントの前の対応する節を参照してください。 この図は、[!DNL server.xml] を完全に表現したものではないことに注意してください。

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
