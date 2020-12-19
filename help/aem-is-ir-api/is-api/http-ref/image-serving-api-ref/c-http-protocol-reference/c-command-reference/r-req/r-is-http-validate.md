---
description: リクエストの検証。
seo-description: リクエストの検証。
seo-title: 検証
solution: Experience Manager
title: 検証
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 5%

---


# 検証{#validate}

リクエストの検証。

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

`req=img`が指定された場合と同じように要求文字列を解析しますが、変数の代入や参照オブジェクト(画像、ICCプロファイル、フォントなど)の評価は行われません。 解析に失敗した場合は標準エラー応答が返され、それ以外の場合は次のプロパティが返されます。

`request.isValid=1`

HTTP応答はキャッシュできません。

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
