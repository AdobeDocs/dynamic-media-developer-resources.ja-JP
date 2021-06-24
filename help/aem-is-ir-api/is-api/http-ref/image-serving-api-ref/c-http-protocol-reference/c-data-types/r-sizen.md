---
description: 正規化サイズ。 画像サイズまたは長方形サイズを指定し、レイヤー0または他の画像のサイズを基準に正規化するために使用します。
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# sizeN{#sizen}

正規化サイズ。 画像サイズまたは長方形サイズを指定し、レイヤー0または他の画像のサイズを基準に正規化するために使用します。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>別の画像を基準にして正規化された幅と高さ（実数、実数、0より大きい値） </p></td> 
 </tr> 
</table>

*nx*&#x200B;と&#x200B;*ny*&#x200B;の両方が0より大きい値である必要があります。 0,0は、特定のデフォルトサイズを使用する必要があることを示している場合があります。 1,1は、参照画像と同じサイズを指定します。
