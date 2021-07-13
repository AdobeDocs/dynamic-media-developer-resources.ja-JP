---
description: メディアセット情報。
solution: Experience Manager
title: セット
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---

# セット{#set}

メディアセット情報。

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコード</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子 </p></td> 
 </tr> 
</table>

URLパスで指定された画像カタログエントリのcatalog::ImageSetに関連付けられた画像、ビデオ、スウォッチ、および様々なメタデータに関する情報を返します。 この応答は、提供されるセットのタイプによって決まる階層構造です。 「xml」または「json」形式が要求された場合は、適切な形式が適用されます。

HTTP応答は、`catalog::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

>[!NOTE]
>
>req=setリクエストでは、コロンは使用できません。

JSON応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
