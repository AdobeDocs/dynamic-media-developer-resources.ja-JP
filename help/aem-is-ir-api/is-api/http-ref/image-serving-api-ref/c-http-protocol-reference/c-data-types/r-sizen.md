---
description: 正規化サイズ レイヤー0などの画像のサイズを基準に正規化された、画像サイズまたは長方形サイズを指定するために使用します。
seo-description: 正規化サイズ レイヤー0などの画像のサイズを基準に正規化された、画像サイズまたは長方形サイズを指定するために使用します。
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

正規化サイズ レイヤー0などの画像のサイズを基準に正規化された、画像サイズまたは長方形サイズを指定するために使用します。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>別の画像を基準とした正規化された幅と高さ（実数、実数、0より大きい） </p></td> 
 </tr> 
</table>

*nx*&#x200B;と&#x200B;*ny*&#x200B;は両方とも0より大きい必要があります。 0,0は、特定のデフォルトサイズを使用する必要があることを示している場合があります。 1,1は、参照画像と同じサイズを指定します。
