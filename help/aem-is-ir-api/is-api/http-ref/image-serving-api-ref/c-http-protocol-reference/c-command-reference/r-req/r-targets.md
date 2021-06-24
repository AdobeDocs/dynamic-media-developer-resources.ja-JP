---
description: 画像カタログのデータをズームターゲットにします。 URLパスで指定された画像カタログエントリのズームターゲットデータを返します。
solution: Experience Manager
title: ターゲット
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# ターゲット{#targets}

画像カタログのデータをズームターゲットにします。 URLパスで指定された画像カタログエントリのズームターゲットデータを返します。

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

`catalog::Targets`の内容が返されます。 「text」形式が要求されると、`catalog::Targets`内の`??`のすべてのインスタンスが行終端子に置き換えられ、1つの行終端子(`CR/LF`)が末尾に追加されます。 URLパスが有効なカタログエントリに解決されない場合、応答は1行のターミネータのみで構成されます。 「xml」または「json」形式が要求された場合は、適切な形式が適用されます。

リクエスト文字列内の他のコマンドは無視されます。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
