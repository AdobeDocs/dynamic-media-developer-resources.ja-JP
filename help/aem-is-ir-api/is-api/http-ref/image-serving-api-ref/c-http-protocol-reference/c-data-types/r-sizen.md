---
description: 正規化されたサイズ： 画像サイズまたは長方形サイズを指定するために使用され、レイヤー0または他の画像のサイズに対して正規化されます。
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
TQID: 'https://experienceleague.adobe.com/QXDv6qIlXZVW050N-6GmKH6PrIiwuN-zzZFuRApBYK4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 0%

---

# sizeN{#sizen}

正規化されたサイズ： 画像サイズまたは長方形サイズを指定するために使用され、レイヤー0または他の画像のサイズに対して正規化されます。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>他の画像に対する正規化された幅と高さ（実数、実数、0より大きい） </p></td> 
 </tr> 
</table>

*nx*&#x200B;と&#x200B;*ny*&#x200B;の両方が0より大きい必要があります。 0,0は、特定のデフォルトサイズを使用する必要があることを示す場合があります。 1,1は、参照画像に等しいサイズを指定します。
