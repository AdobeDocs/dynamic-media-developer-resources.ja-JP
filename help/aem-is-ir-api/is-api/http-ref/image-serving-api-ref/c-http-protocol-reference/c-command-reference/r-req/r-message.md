---
description: クライアントメッセージ。 クライアントがサーバーログに短いテキストメッセージを挿入するメカニズムを提供します。
seo-description: クライアントメッセージ。 クライアントがサーバーログに短いテキストメッセージを挿入するメカニズムを提供します。
seo-title: message
solution: Experience Manager
title: message
topic: Scene7 Image Serving - Image Rendering API
uuid: 38d6d0e7-55cf-43ea-85b7-8f4aade4208a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# message{#message}

クライアントメッセージ。 クライアントがサーバーログに短いテキストメッセージを挿入するメカニズムを提供します。

`req=message&message= *`文字列`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 文字列</span> </p> </td> 
  <td class="stentry"> <p>メッセージ文字列。 </p></td> 
 </tr> 
</table>

HTTP応答はキャッシュできません。 空の応答がMIMEタイプと共に返されま `text/plain`す。
