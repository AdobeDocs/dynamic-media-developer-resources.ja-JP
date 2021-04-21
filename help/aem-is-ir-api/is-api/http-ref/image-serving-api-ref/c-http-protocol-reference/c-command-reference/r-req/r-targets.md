---
description: 画像カタログのターゲットデータをズームします。 URLパスで指定された画像カタログエントリのズームターゲットデータを返します。
solution: Experience Manager
title: ターゲット
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---


# ターゲット{#targets}

画像カタログのターゲットデータをズームします。 URLパスで指定された画像カタログエントリのズームターゲットデータを返します。

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

`catalog::Targets`の内容が返されます。 &#39;text&#39;形式が要求されると、`catalog::Targets`内の`??`のすべてのインスタンスは行終端子に置き換えられ、末尾に1つの行終端子(`CR/LF`)が追加されます。 URLパスが有効なカタログエントリに解決されない場合、応答には1つの行終端子のみが含まれます。 「xml」または「json」形式が要求された場合、適切な形式設定が適用されます。

要求文字列内の他のコマンドは無視されます。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
