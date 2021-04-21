---
description: 正規化サイズ レイヤー0などの画像のサイズを基準に正規化された、画像サイズまたは長方形サイズを指定するために使用します。
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
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
