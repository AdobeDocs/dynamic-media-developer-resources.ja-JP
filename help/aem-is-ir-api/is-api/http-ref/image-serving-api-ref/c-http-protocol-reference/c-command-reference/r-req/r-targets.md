---
description: ズームターゲットのデータを画像カタログから取得します。 URL パスで指定された画像カタログエントリのズームターゲットデータを返します。
solution: Experience Manager
title: ターゲット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# ターゲット{#targets}

ズームターゲットのデータを画像カタログから取得します。 URL パスで指定された画像カタログエントリのズームターゲットデータを返します。

`req=targets[,text|{xml[, *`エンコード`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

次の内容： `catalog::Targets` が返されます。 &#39;text&#39;形式がリクエストされた場合、 `??` in `catalog::Targets` はラインターミネータと 1 行ターミネータ ( `CR/LF`) が末尾に追加されます。 URL パスが有効なカタログエントリに解決されない場合、応答は 1 行のターミネータのみで構成されます。 「xml」または「json」形式が要求された場合は、適切な形式が適用されます。

リクエスト文字列内の他のコマンドは無視されます。

HTTP 応答は、TTL に基づいてキャッシュ可能です。 `catalog::Expiration`.

JSONP 応答形式をサポートするリクエストでは、の拡張構文を使用して JS コールバックハンドラーの名前を指定できます。 `req=` パラメーター：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみ使用できます。 オプション。初期設定は `s7jsonResponse`.
