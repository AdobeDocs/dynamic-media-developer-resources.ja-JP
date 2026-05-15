---
description: メディアセット情報：
solution: Experience Manager
title: セット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
TQID: 'https://experienceleague.adobe.com/nfNdFeRk7TDhSYHdy05x6fxNKMBhTF7f11xoji13VP4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 144
ht-degree: 2%

---

# セット{#set}

メディアセット情報：

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコーディング </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト ID </p></td> 
 </tr> 
</table>

URL パスで指定された画像カタログエントリのcatalog::ImageSetに関連する画像、ビデオ、スウォッチ、および様々なメタデータに関する情報を返します。 この応答は、提供されるセットのタイプによって決定される階層構造です。 「xml」または「json」形式が要求された場合、適切な形式が適用されます。

HTTP応答は、`catalog::NonImgExpiration`に基づくTTLでキャッシュできます。

>[!NOTE]
>
>req=set リクエストでは、コロン文字は使用できません。

JSON応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。
