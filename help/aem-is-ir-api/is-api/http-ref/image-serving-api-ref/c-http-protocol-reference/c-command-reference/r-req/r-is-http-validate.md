---
description: リクエストの検証。
solution: Experience Manager
title: 検証
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

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

は、変数を置き換えたり、参照され `req=img` オブジェクト（画像、ICC プロファイル、フォントなど）を評価したりせずに、リクエスト文字列を指定されたかのように解析します。 解析が失敗した場合は、標準のエラー応答が返されます。それ以外の場合は、次のプロパティが返されます。

`request.isValid=1`

HTTP 応答はキャッシュできません。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。
