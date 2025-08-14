---
description: マルチビットレートデータ。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

マルチビットレートデータ。

`req=mbrSet[,text|xml[, *`encoding`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコーディング </span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

ネットパス ID に関連付けられたビデオセット内の有効なビデオエントリに対応する URL （および対応するビットレート）のリストを含む、テキストまたは xml 応答を返します。

有効なビデオエントリに `catalog::VideoBitRate` の値が含まれているという以前の要件が緩和されました。 エントリには `catalog::VideoBitRate`*or*`catalog::AudioBitRate`*or* `catalog::TotalStreamBitRate` の値を含めることができます。 ビデオエントリを有効にするには、これらのうち 1 つだけを定義する必要があります。 `catalog::Path` と有効なビデオファイル拡張子の要件は変更されていません。

応答は、Appleおよび Flash ストリーミングサーバーでの使用を目的としているので、これらの仕様に構造的に準拠しています。 URL は、プレフィックス `attribute::HttpAppleStreamingContext` および `attribute::HttpFlashStreamingContext` を使用して生成されます。

m3u8 の応答には、ビデオセットに mp4 ファイルが存在する場合にのみ mp4 ファイルが含まれます。 mp4 ファイルが存在しない場合、これらの応答には f4v ファイルのみが含まれます。 mp4 ファイルも f4v ファイルも存在しない場合、応答は空になります。

f4m 応答には、ビデオセットに f4v ファイルが存在する場合のみ含まれます。 f4v ファイルが存在しない場合、これらの応答には mp4 ファイルのみが含まれます。 f4v ファイルも mp4 ファイルも存在しない場合、応答は空になります。

f4m/m3u8 応答に表示されるビットレートは、`catalog::TotalStreamBitRate` の値（適切な単位に変換されたもの）に対応しています。 `catalog::TotalStreamBitRate` が定義されていない場合、`catalog::VideoBitRate` と `catalog::AudioBitRate` の合計が使用されます。

HTTP 応答は、`catalog::NonImgExpiration` に基づく TTL でキャッシュ可能です。
