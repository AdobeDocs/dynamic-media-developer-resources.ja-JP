---
description: リクエストの検証：
solution: Experience Manager
title: 検証
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
TQID: 'https://experienceleague.adobe.com/TfgOIjG2q1CKAulErZYftqmKnCocuSF-H-dQTj4xsFI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 105
ht-degree: 2%

---

# 検証{#validate}

リクエストの検証：

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト ID。 </p></td> 
 </tr> 
</table>

`req=img`が指定されたかのようにリクエスト文字列を解析しますが、変数を代入したり、参照オブジェクト（画像、ICC プロファイル、フォントなど）を評価したりすることはありません。 解析が失敗した場合は、標準のエラー応答が返されます。それ以外の場合は、次のプロパティが返されます。

`request.isValid=1`

HTTP応答はキャッシュできません。

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。
