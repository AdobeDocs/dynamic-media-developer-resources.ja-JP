---
description: プラットフォームサーバーの設定が含まれます。
solution: Experience Manager
title: server.xml
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# server.xml{#server-xml}

プラットフォームサーバーの設定が含まれます。

このXMLファイルを変更する場合は、有効なXML構文を維持するように注意する必要があります。そうしないと、プラットフォームサーバーで開始が失敗する場合があります。

変更を有効にするには、このファイルを編集した後でプラットフォームサーバーを再起動する必要があります。

次の図に、このファイルで変更できる設定を示します。 これらの設定の説明は、このドキュメントの前の対応する節を参照してください。 この図は[!DNL server.xml]の完全な表現ではないことに注意してください。

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

