---
title: coordN
description: 正規化された座標。 画像のサイズに合わせて正規化された、画像のオフセットや切り抜きパラメーターなど、画像内の相対的な位置を指定するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
TQID: 'https://experienceleague.adobe.com/-dtYByOGK-mNAWc0yQBs4nu5sO1r-Ormq70iwdDZBjg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# coordN{#coordn}

正規化された座標。 画像のサイズに合わせて正規化された、画像のオフセットや切り抜きパラメーターなど、画像内の相対的な位置を指定するために使用します。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>画像サイズに正規化された座標オフセット（実数、実数） </p></td> 
 </tr> 
</table>

正の値は右下に移動します。

多くの場合、参照位置は画像の中心です。 この場合、`0,0`は画像の中心、`-0.5,-0.5`は左上隅、`0.5,0.5`は右下隅に対応します。

また、レイヤー0のサイズに対する画像サイズまたは長方形サイズを指定する場合にも使用します。 この場合、値は0より大きくなければなりません。 0は、特定のデフォルト値を使用する必要があることを示します。 値`1,1`は、レイヤー0と同じサイズを指定します。
