---
description: 画像カタログのユーザデータ。 URL パスで指定された画像カタログエントリのユーザーデータを返します。
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---

# userdata{#userdata}

画像カタログのユーザデータ。 URL パスで指定された画像カタログエントリのユーザーデータを返します。

`req=userdata[,text|{xml[, *`エンコード`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコード</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

次の内容： `catalog::UserData` が返されます。 &#39;text&#39;形式を指定した場合、 `??` in `catalog::UserData`は行終端子に置き換えられ、1 行終端子 (CR/LF) が末尾に追加されます。 URL パスが有効なカタログエントリに解決されない場合、応答は 1 行のターミネータのみで構成されます。 「xml」または「json」形式が要求された場合は、適切な形式が適用されます。

リクエスト文字列内の他のコマンドは無視されます。

HTTP 応答は、TTL に基づいてキャッシュ可能です。 `catalog::Expiration`.

>[!NOTE]
>
>userdata プロパティのキー名でコロンは使用できません。

JSONP 応答形式をサポートするリクエストでは、の拡張構文を使用して JS コールバックハンドラーの名前を指定できます。 `req=` パラメーター：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみ使用できます。 オプション。初期設定は `s7jsonResponse`.
