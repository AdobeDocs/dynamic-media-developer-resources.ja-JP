---
description: マルチビットレートデータ。
seo-description: マルチビットレートデータ。
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mbrSet{#mbrset}

マルチビットレートデータ。

`req=mbrSet[,text|xml[, *`encodingfmtType`*]][&fmt= *``*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m| m3u8</span> </p></td> 
 </tr> 
</table>

ネットパスIDに関連付けられたビデオセット内の有効なビデオエントリに対応するURL（および対応するビットレート）のリストを含むテキストまたはxml応答を返します。

以前は、有効なビデオエントリにの値を含めるという要件が緩和 `catalog::VideoBitRate` されていました。 エントリには、またはの値を含める `catalog::VideoBitRate`*こと&#x200B;*ができます`catalog::AudioBitRate`**`catalog::TotalStreamBitRate`。 ビデオエントリを有効にするには、これらのうち1つのみを定義する必要があります。 有効なビデオファイル拡張子 `catalog::Path` との要件は変更されていません。

応答は、AppleおよびFlash Streaming Serverでの消費を目的としており、これらの仕様に構造的に準拠しています。 URLは、プリフィックスとを使用して生 `attribute::HttpAppleStreamingContext` 成されま `attribute::HttpFlashStreamingContext`す。

m3u8応答には、ビデオセットにmp4ファイルが存在する場合にのみ含まれます。 mp4ファイルが存在しない場合、これらの応答にはf4vファイルのみが含まれます。 mp4ファイルもf4vファイルも存在しない場合、応答は空です。

f4m応答には、ビデオセットにf4vファイルが存在する場合にのみf4vファイルが含まれます。 f4vファイルが存在しない場合、これらの応答にはmp4ファイルのみが含まれます。 f4vファイルもmp4ファイルも存在しない場合、応答は空です。

f4m/m3u8応答で表示されるビットレートは、の値に対応します(適 `catalog::TotalStreamBitRate` 切な単位に変換されます)。 を定義 `catalog::TotalStreamBitRate` しない場合、との合計が `catalog::VideoBitRate` 使用 `catalog::AudioBitRate` されます。

The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.
