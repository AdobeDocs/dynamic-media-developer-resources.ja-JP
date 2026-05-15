---
description: 画像カタログからのユーザーデータ。 url パスで指定された画像カタログエントリのユーザーデータを返します。
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
TQID: 'https://experienceleague.adobe.com/cLVsaN--jydZTkV6GA92jN1PO8VOFAEZxhSg7F2S9dk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# userdata{#userdata}

画像カタログからのユーザーデータ。 url パスで指定された画像カタログエントリのユーザーデータを返します。

`req=userdata[,text|{xml[, *` エンコーディング `*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> エンコーディング </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

`catalog::UserData`の内容が返されます。 「テキスト」形式を指定すると、`catalog::UserData`内の`??`のすべてのインスタンスが行ターミネータに置き換えられ、最後に単行終端（CR/LF）が追加されます。 URL パスが有効なカタログ エントリに解決されない場合、応答は1行のターミネータのみで構成されます。 「xml」または「json」形式が要求された場合、適切な形式が適用されます。

リクエスト文字列内のその他のコマンドは無視されます。

HTTP応答は、`catalog::Expiration`に基づくTTLでキャッシュできます。

>[!NOTE]
>
>userdata プロパティキー名では、コロン文字は使用できません。

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。
