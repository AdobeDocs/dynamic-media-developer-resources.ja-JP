---
description: 画像カタログのユーザデータ。 URLパスで指定された画像カタログエントリのユーザデータを返します。
seo-description: 画像カタログのユーザデータ。 URLパスで指定された画像カタログエントリのユーザデータを返します。
seo-title: userdata
solution: Experience Manager
title: userdata
topic: Scene7 Image Serving - Image Rendering API
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 2%

---


# userdata{#userdata}

画像カタログのユーザデータ。 URLパスで指定された画像カタログエントリのユーザデータを返します。

`req=userdata[,text|{xml[, *`エンコード`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコード</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

`catalog::UserData`の内容が返されます。 &#39;text&#39;形式を指定すると、`catalog::UserData`内の`??`のすべてのインスタンスが行終端子に置き換えられ、末尾に1つの行終端子(CR/LF)が追加されます。 URLパスが有効なカタログエントリに解決されない場合、応答には1つの行終端子のみが含まれます。 「xml」または「json」形式が要求された場合、適切な形式設定が適用されます。

要求文字列内の他のコマンドは無視されます。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。

>[!NOTE]
>
>userdataプロパティのキー名にコロンは使用できません。

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.
