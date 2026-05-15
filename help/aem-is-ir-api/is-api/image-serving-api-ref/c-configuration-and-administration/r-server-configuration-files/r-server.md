---
description: プラットフォームサーバー設定が含まれます。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
TQID: 'https://experienceleague.adobe.com/XBxGVJnRV-RYoKBJD5-Q6qiIhwIAJKzus53izIHokfs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 0%

---

# server.xml{#server-xml}

プラットフォームサーバー設定が含まれます。

このXML ファイルを変更する場合は、有効なXML構文を維持するように注意する必要があります。そうしないと、[!DNL Platform Server]を開始できない可能性があります。

変更を有効にするには、このファイルを編集した後で[!DNL Platform Server]を再起動する必要があります。

次の図は、このファイルで変更できる設定を示しています。 これらの設定について詳しくは、このドキュメントの前述の対応するセクションを参照してください。 この図は、[!DNL server.xml]の完全な表現ではありません。

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
