---
description: ズームターゲット画像カタログのデータ URLパスで指定された画像カタログエントリのズームターゲットデータを返します。
seo-description: ズームターゲット画像カタログのデータ URLパスで指定された画像カタログエントリのズームターゲットデータを返します。
seo-title: ターゲット
solution: Experience Manager
title: ターゲット
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ターゲット{#targets}

ズームターゲット画像カタログのデータ URLパスで指定された画像カタログエントリのズームターゲットデータを返します。

`req=targets[,text|{xml[, *`encodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

の内容が返 `catalog::Targets` されます。 &#39;text&#39;形式が要求されると、 `??` inのすべてのインスタ `catalog::Targets` ンスが行終端子に置き換えられ、1つの行終端文字( `CR/LF`)が末尾に追加されます。 URLパスが有効なカタログエントリに解決されない場合、応答は1つの行終端文字のみで構成されます。 「xml」または「json」形式が要求された場合、適切な形式が適用されます。

要求文字列内の他のコマンドは無視されます。

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

JSONP応答形式をサポートするリクエストを使用すると、次のパラメーターの拡張構文を使用してJSコールバックハンドラーの名前を指定で `req=` きます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。 a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
