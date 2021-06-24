---
description: マルチビットレートデータ。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '264'
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

以前の有効なビデオエントリに`catalog::VideoBitRate`の値が含まれるという要件は緩和されました。 エントリには、`catalog::VideoBitRate`*または* `catalog::AudioBitRate`*または* `catalog::TotalStreamBitRate`の値を含めることができます。 ビデオエントリが有効であるために定義する必要があるのは、これらのうちの1つだけです。 `catalog::Path`と有効なビデオファイル拡張子の要件は変わっていません。

応答は、AppleおよびFlashストリーミングサーバーでの使用を目的としており、構造的にこれらの仕様に準拠しています。 URLは、プレフィックス`attribute::HttpAppleStreamingContext`と`attribute::HttpFlashStreamingContext`を使用して生成されます。

m3u8応答には、ビデオセット内にmp4ファイルが存在する場合にのみmp4ファイルが含まれます。 mp4ファイルが存在しない場合、これらの応答にはf4vファイルのみが含まれます。 mp4ファイルもf4vファイルも存在しない場合、応答は空になります。

f4m応答には、ビデオセットにf4vファイルが存在する場合にのみ、f4vファイルが含まれます。 f4vファイルが存在しない場合、これらの応答にはmp4ファイルのみが含まれます。 f4vファイルもmp4ファイルも存在しない場合、応答は空になります。

f4m/m3u8応答で表示されるビットレートは、`catalog::TotalStreamBitRate`の値に対応します（適切な単位に変換）。 `catalog::TotalStreamBitRate`を定義しない場合は、`catalog::VideoBitRate`と`catalog::AudioBitRate`の合計が使用されます。

HTTP応答は、`catalog::NonImgExpiration`に基づいてTTLでキャッシュ可能です。
