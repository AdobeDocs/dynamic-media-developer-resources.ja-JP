---
description: プラットフォームサーバーの設定が含まれます。
seo-description: プラットフォームサーバーの設定が含まれます。
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '89'
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

