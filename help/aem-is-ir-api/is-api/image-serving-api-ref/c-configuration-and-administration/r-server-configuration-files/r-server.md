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

---


# server.xml{#server-xml}

プラットフォームサーバーの設定が含まれます。

このXMLファイルを変更する場合、有効なXML構文を維持するように注意する必要があります。そうしないと、プラットフォームサーバーの起動に失敗する可能性があります。

変更を有効にするには、このファイルを編集した後で、プラットフォームサーバーを再起動する必要があります。

次の図に、このファイルで変更できる設定を示します。 これらの設定の説明は、このドキュメントの前述の対応するセクションを参照してください。 この図はの完全な表現ではありませ [!DNL server.xml]ん。

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

