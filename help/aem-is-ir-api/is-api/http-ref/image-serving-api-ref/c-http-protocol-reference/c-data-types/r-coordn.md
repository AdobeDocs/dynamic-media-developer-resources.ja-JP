---
title: coordN
description: 正規化された座標。 画像のサイズに正規化された、画像内の相対位置（画像オフセットや切り抜きパラメーターなど）を指定するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# coordN{#coordn}

正規化された座標。 画像のサイズに正規化された、画像内の相対位置（画像オフセットや切り抜きパラメーターなど）を指定するために使用します。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>画像のサイズに正規化された座標オフセット（実数、実数） </p></td> 
 </tr> 
</table>

正の値は右下に向かって移動します。

多くの場合、参照位置は画像の中心です。 この場合、`0,0` は画像の中心、左上隅、右下隅に `-0.5,-0.5` 致 `0.5,0.5` ます。

また、レイヤー 0 のサイズに対する画像サイズまたは長方形サイズの指定にも使用されます。 この場合、値は 0 より大きい値にする必要があります。 0 は、特定のデフォルト値を使用する必要があることを示す場合があります。 値が `1,1` の場合は、レイヤ 0 のサイズと等しいサイズが指定されます。
