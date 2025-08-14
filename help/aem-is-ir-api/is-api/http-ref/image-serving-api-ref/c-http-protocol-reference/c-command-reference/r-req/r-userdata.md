---
description: 画像カタログのユーザーデータ。 URL パスで指定された画像カタログエントリのユーザーデータを返します。
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# userdata{#userdata}

画像カタログのユーザーデータ。 URL パスで指定された画像カタログエントリのユーザーデータを返します。

`req=userdata[,text|{xml[, *` エンコード `*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコーディング </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

`catalog::UserData` のコンテンツが返されます。 「text」フォーマットを指定すると、`??` 内の `catalog::UserData` のすべてのインスタンスが行終端文字に置き換えられ、単一行終端文字（CR/LF）が末尾に追加されます。 URL パスが有効なカタログエントリに解決されない場合、応答は 1 行のターミネータのみで構成されます。 「xml」または「json」形式がリクエストされた場合、適切なフォーマットが適用されます。

リクエスト文字列内のその他のコマンドは無視されます。

HTTP 応答は、`catalog::Expiration` に基づく TTL でキャッシュ可能です。

>[!NOTE]
>
>userdata プロパティのキー名にコロン文字は使用できません。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。
