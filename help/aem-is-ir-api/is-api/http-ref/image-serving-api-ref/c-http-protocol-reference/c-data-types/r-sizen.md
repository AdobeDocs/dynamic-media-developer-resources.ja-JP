---
description: 正規化されたサイズ レイヤー0または他の画像のサイズを基準にして正規化された、画像サイズまたは長方形サイズを指定するために使用します。
seo-description: 正規化されたサイズ レイヤー0または他の画像のサイズを基準にして正規化された、画像サイズまたは長方形サイズを指定するために使用します。
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sizeN{#sizen}

正規化されたサイズ レイヤー0または他の画像のサイズを基準にして正規化された、画像サイズまたは長方形サイズを指定するために使用します。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> , ny </span><span class="codeph"><span class="varname"></span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> , ny </span><span class="codeph"><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>別の画像を基準とした正規化された幅と高さ（実数、実数、0より大きい） </p></td> 
 </tr> 
</table>

nxと *nyは* 、両方と *も* 0より大きい値にする必要があります。 0,0は、特定のデフォルトサイズを使用することを示している場合があります。 1,1は、参照画像と同じサイズを指定します。
