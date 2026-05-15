---
description: 画像カタログの画像セットデータ。 URL パスで指定された画像カタログエントリの画像セットデータを返します。
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
TQID: 'https://experienceleague.adobe.com/1PbZjs--lk7GcyXU1F-AJ-vWcgwVX9JFivvbnTGrWKQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# imageset{#imageset}

画像カタログの画像セットデータ。 URL パスで指定された画像カタログエントリの画像セットデータを返します。

`req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコーディング </span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト ID。 </p></td> 
 </tr> 
</table>

`catalog::ImageSet`のコンテンツは、それ以上の変更を加えずに返され（文字列ローカライズを除く、該当する場合）、その後に1行のターミネーター（CR/LF）が続きます。 URL パスが有効なカタログ エントリに解決されない場合、応答は1行のターミネータのみで構成されます。

リクエスト文字列内のその他のコマンドは無視されます。 HTTP応答は、`catalog::NonImgExpiration`に基づくTTLでキャッシュできます。

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。
