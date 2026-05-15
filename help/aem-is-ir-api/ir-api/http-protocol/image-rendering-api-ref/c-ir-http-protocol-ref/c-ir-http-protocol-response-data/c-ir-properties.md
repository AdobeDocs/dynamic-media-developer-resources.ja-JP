---
title: プロパティ
description: プロパティデータは、次のreq=型imagepropsおよびpropに応答して返されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
TQID: 'https://experienceleague.adobe.com/AIeKRT2-o9Z35SjXjrGECIWHFLRrdJz5JO-CkCOLj8U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# プロパティ{#properties}

プロパティデータは、次のreq=型に応答して返されます：imagepropsとprops。

返信データは、Java™ プロパティとして読み取り可能な形式になっています。 一般的なテキストプロパティの応答には、次の一般的な構造があります。

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*`は空にできます。 空白文字は、各行の先頭と末尾、および&#39;=&#39;区切り記号の前後でオプションです。 文字列の値を囲むには、一重引用符または二重引用符を使用できますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`、`\\`などのJAVA スタイルのエスケープ文字を含めることができます。

**関連項目**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
