---
description: Zoomは画像カタログのデータをターゲットにします。 URL パスで指定された画像カタログエントリのズームターゲットデータを返します。
solution: Experience Manager
title: ターゲット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
TQID: 'https://experienceleague.adobe.com/3JPTLaprpB2W2G-ua8CxAOShG3C7kinQB5u12Dv29bQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 188
ht-degree: 1%

---

# ターゲット{#targets}

Zoomは画像カタログのデータをターゲットにします。 URL パスで指定された画像カタログエントリのズームターゲットデータを返します。

`req=targets[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト ID。 </p></td> 
 </tr> 
</table>

`catalog::Targets`の内容が返されます。 「テキスト」形式が要求されると、`catalog::Targets`内の`??`のすべてのインスタンスが行ターミネータに置き換えられ、最後に1行ターミネータ（`CR/LF`）が追加されます。 URL パスが有効なカタログ エントリに解決されない場合、応答は1行のターミネータのみで構成されます。 「xml」または「json」形式が要求された場合、適切な形式が適用されます。

リクエスト文字列内のその他のコマンドは無視されます。

HTTP応答は、`catalog::Expiration`に基づくTTLでキャッシュできます。

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。
