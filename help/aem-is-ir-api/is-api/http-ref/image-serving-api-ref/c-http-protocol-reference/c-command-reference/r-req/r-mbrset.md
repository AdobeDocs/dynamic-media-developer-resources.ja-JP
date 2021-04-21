---
description: マルチビットレートデータ。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# mbrSet{#mbrset}

マルチビットレートデータ。

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

ネットパスIDに関連付けられたビデオセット内の有効なビデオエントリに対応するURL（および対応するビットレート）のリストを含むテキストまたはxml応答を返します。

以前、有効なビデオエントリに`catalog::VideoBitRate`の値を含めるという要件は緩和されました。 エントリには、`catalog::VideoBitRate`*または* `catalog::AudioBitRate`*または* `catalog::TotalStreamBitRate`の値を含めることができます。 ビデオエントリを有効にするには、これらのうち1つのみを定義する必要があります。 `catalog::Path`と有効なビデオファイル拡張子に関する要件は変更されていません。

応答は、AppleおよびFlashストリーミングサーバーでの消費を目的としており、構造的にはこれらの仕様に準拠しています。 URLは、プリフィックス`attribute::HttpAppleStreamingContext`と`attribute::HttpFlashStreamingContext`を使用して生成されます。

m3u8応答には、mp4ファイル（ビデオセットに存在する場合）のみが含まれます。 mp4ファイルがない場合、これらの応答にはf4vファイルのみが含まれます。 mp4ファイルもf4vファイルも存在しない場合、応答は空です。

f4m応答には、f4vファイルが含まれる（ビデオセットに存在する場合）限り、f4vファイルが含まれます。 f4vファイルがない場合、これらの応答にはmp4ファイルのみが含まれます。 f4vファイルもmp4ファイルも存在しない場合、応答は空です。

f4m/m3u8応答に表示されるビットレートは、`catalog::TotalStreamBitRate`の値に対応します（適切な単位に変換されます）。 `catalog::TotalStreamBitRate`を定義しない場合は、`catalog::VideoBitRate`と`catalog::AudioBitRate`の合計が使用されます。

HTTP応答は、`catalog::NonImgExpiration`に基づいてTTLでキャッシュ可能です。
