---
description: 画像カタログの画像セットデータ。 URL パスで指定された画像カタログエントリの画像セットデータを返します。
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# imageset{#imageset}

画像カタログの画像セットデータ。 URL パスで指定された画像カタログエントリの画像セットデータを返します。

`req=imageset[,text|javascript|{xml[, *`エンコード`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

の内容 `catalog::ImageSet` がそれ以上変更されずに返されます（文字列のローカライゼーションが可能な場合はそれ以外）。その後に 1 行のターミネータ (CR/LF) が続きます。 URL パスが有効なカタログエントリに解決されない場合、応答は 1 行のターミネータのみで構成されます。

リクエスト文字列内の他のコマンドは無視されます。 HTTP 応答は、TTL に基づいてキャッシュ可能です。 `catalog::NonImgExpiration`.

JSONP 応答形式をサポートするリクエストでは、の拡張構文を使用して JS コールバックハンドラーの名前を指定できます。 `req=` パラメーター：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみ使用できます。 オプション。初期設定は `s7jsonResponse`.
