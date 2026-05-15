---
description: マルチビットレートデータ：
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
TQID: 'https://experienceleague.adobe.com/j8HXFZEv-TJINp20XNewqo82k-Yy39Aey4FU4Tm8AVc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 253
ht-degree: 0%

---

# mbrSet{#mbrset}

マルチビットレートデータ：

`req=mbrSet[,text|xml[, *` エンコーディング `*]][&fmt= *`fmtType`*]`

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

ネットパス IDに関連付けられたビデオセット内の有効なビデオエントリに対応するURL （および対応するビットレート）のリストを含むテキストまたはxml応答を返します。

有効なビデオエントリに`catalog::VideoBitRate`の値が含まれているという以前の要件が緩和されました。 エントリには、`catalog::VideoBitRate`*または* `catalog::AudioBitRate`*または* `catalog::TotalStreamBitRate`の値を含めることができます。 ビデオエントリを有効にするには、これらのいずれかを定義する必要があります。 `catalog::Path`と有効なビデオファイル拡張子の要件は変更されていないことに注意してください。

応答は、AppleおよびFlash ストリーミングサーバーによる使用を目的としているため、これらの仕様に構造的に準拠しています。 URLは、接頭辞`attribute::HttpAppleStreamingContext`と`attribute::HttpFlashStreamingContext`を使用して生成されます。

m3u8応答には、ビデオセットに存在するmp4 ファイルのみが含まれます。 mp4 ファイルが存在しない場合、これらの応答にはf4v ファイルのみが含まれます。 mp4 ファイルもf4v ファイルも存在しない場合、応答は空になります。

f4m応答には、ビデオセットにf4v ファイルが存在する場合にのみ含まれます。 f4v ファイルが存在しない場合、これらの応答にはmp4 ファイルのみが含まれます。 f4v ファイルもmp4 ファイルも存在しない場合、応答は空になります。

f4m/m3u8応答に表示されるビットレートは、`catalog::TotalStreamBitRate`の値（適切な単位に変換）に対応します。 `catalog::TotalStreamBitRate`が定義されていない場合、`catalog::VideoBitRate`と`catalog::AudioBitRate`の合計が使用されます。

HTTP応答は、`catalog::NonImgExpiration`に基づくTTLでキャッシュできます。
