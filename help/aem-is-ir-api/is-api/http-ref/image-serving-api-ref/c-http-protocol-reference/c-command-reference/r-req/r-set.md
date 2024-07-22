---
description: メディアセット情報。
solution: Experience Manager
title: セット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# セット{#set}

メディアセット情報。

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコーディング </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子 </p></td> 
 </tr> 
</table>

URL パスで指定された画像カタログエントリの catalog::ImageSet に関連付けられた画像、ビデオ、スウォッチ、および様々なメタデータに関する情報を返します。 この応答は、提供されたセットのタイプによって決定される階層構造です。 「xml」または「json」形式がリクエストされた場合、適切なフォーマットが適用されます。

HTTP 応答は、`catalog::NonImgExpiration` に基づく TTL でキャッシュ可能です。

>[!NOTE]
>
>req=set リクエストではコロン文字は使用できません。

JSON 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。
