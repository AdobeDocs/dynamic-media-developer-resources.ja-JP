---
description: 画像カタログのプロパティ。 要求パスで指定された画像カタログの共通属性を返します。
solution: Experience Manager
title: catalogprops
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 6%

---


# catalogprops{#catalogprops}

画像カタログのプロパティ。 要求パスで指定された画像カタログの共通属性を返します。

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

デフォルトのカタログプロパティ([!DNL default.ini])を取得するには、カタログIDを省略します。 HTTP応答は、`attribute::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

次のプロパティ値が返されます。

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ</b> </td> 
   <td> <b> 種類</b> </td> 
   <td> <b> 対応するカタログ属性</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> <span class="codeph"> attribute::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::defaultExt</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> attribute::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> attribute::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> attribute::LastModified</span>(存在しない場合は <span class="varname"> catalog</span><span class="filepath"> .</span> inifileの最終変更時刻) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph"> attribute::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> attribute::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> attribute::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> attribute::ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::watermark</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> attribute::Watermark</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

