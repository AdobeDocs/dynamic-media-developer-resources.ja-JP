---
description: メディアセット情報
seo-description: メディアセット情報
seo-title: セット
solution: Experience Manager
title: セット
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---


# セット{#set}

メディアセット情報

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコード</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>一意の要求識別子 </p></td> 
 </tr> 
</table>

URLパスで指定された画像カタログエントリに対して、catalog::ImageSetに関連付けられた画像、ビデオ、スウォッチ、および様々なメタデータに関する情報を返します。 この応答は、提供されたセットのタイプによって決まる階層構造です。 「xml」または「json」形式が要求された場合、適切な形式設定が適用されます。

HTTP応答は、`catalog::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

>[!NOTE]
>
>req=setリクエストでは、コロン文字は使用できません。

JSON応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用してJSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
