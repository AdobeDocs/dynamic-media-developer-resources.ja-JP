---
description: 画像カタログのズームターゲットデータ。 URL パスで指定された画像カタログエントリのズームターゲットデータを返します。
solution: Experience Manager
title: ターゲット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# ターゲット{#targets}

画像カタログのズームターゲットデータ。 URL パスで指定された画像カタログエントリのズームターゲットデータを返します。

`req=targets[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

`catalog::Targets` のコンテンツが返されます。 「text」フォーマットが要求されると、`catalog::Targets` の `??` のインスタンスはすべて行終端文字に置き換えられ、1 行の終端文字（`CR/LF`）が末尾に追加されます。 URL パスが有効なカタログエントリに解決されない場合、応答は 1 行のターミネータのみで構成されます。 「xml」または「json」形式がリクエストされた場合、適切なフォーマットが適用されます。

リクエスト文字列内のその他のコマンドは無視されます。

HTTP 応答は、`catalog::Expiration` に基づく TTL でキャッシュ可能です。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。
