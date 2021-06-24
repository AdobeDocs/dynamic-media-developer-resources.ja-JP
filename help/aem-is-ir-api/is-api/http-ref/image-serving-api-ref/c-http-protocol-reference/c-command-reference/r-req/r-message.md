---
description: クライアントメッセージ。 クライアントが短いテキストメッセージをサーバーログに挿入するメカニズムを提供します。
solution: Experience Manager
title: message
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 47e51181-714c-4b25-a375-f3b2238cd534
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# メッセージ{#message}

クライアントメッセージ。 クライアントが短いテキストメッセージをサーバーログに挿入するメカニズムを提供します。

`req=message&message= *`文字列`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 文字列</span> </p> </td> 
  <td class="stentry"> <p>メッセージ文字列。 </p></td> 
 </tr> 
</table>

HTTP応答はキャッシュできません。 空の応答はMIMEタイプ`text/plain`で返されます。
