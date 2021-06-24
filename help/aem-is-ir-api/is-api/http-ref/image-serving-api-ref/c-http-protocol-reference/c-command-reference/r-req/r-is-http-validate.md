---
description: リクエストの検証。
solution: Experience Manager
title: 検証
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# 検証{#validate}

リクエストの検証。

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

リクエスト文字列を`req=img`が指定された場合と同じように解析しますが、変数を置き換えたり、参照オブジェクト（画像、ICCプロファイル、フォントなど）を評価したりする必要はありません。 解析が失敗した場合は標準エラー応答が返され、失敗した場合は次のプロパティが返されます。

`request.isValid=1`

HTTP応答はキャッシュできません。

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
