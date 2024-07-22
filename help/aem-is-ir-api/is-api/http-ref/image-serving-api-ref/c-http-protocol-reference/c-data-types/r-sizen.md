---
description: 正規化されたサイズ 画像サイズまたは長方形サイズを指定するために使用します。レイヤー 0 またはその他の画像のサイズに対して正規化されます。
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# sizeN{#sizen}

正規化されたサイズ 画像サイズまたは長方形サイズを指定するために使用します。レイヤー 0 またはその他の画像のサイズに対して正規化されます。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>別の画像を基準に正規化された幅と高さ（実数、実数、0 より大きい） </p></td> 
 </tr> 
</table>

*nx* と *ny* はどちらも 0 より大きくなければなりません。 0,0 は、特定のデフォルトサイズを使用する必要があることを示す場合があります。 1,1 は、参照画像と等しいサイズを指定します。
