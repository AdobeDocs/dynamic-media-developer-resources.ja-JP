---
title: 座標
description: ピクセル座標。 画像の座標を、画像またはレイヤーの長方形の左上隅を基準としたピクセルオフセットの形式で指定する場合に使用します。 これらの座標は、多くの場合、画像のオフセットや切り抜きパラメーターで使用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12ca4002-a540-4eb9-bb11-824d7cb41d30
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# 座標{#coord}

ピクセル座標。 画像の座標を、画像またはレイヤーの長方形の左上隅を基準としたピクセルオフセットの形式で指定する場合に使用します。 これらの座標は、多くの場合、画像のオフセットや切り抜きパラメーターで使用されます。

<table id="simpletable_A686120953124ACB8803CB9C877252AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> px</span> </span>, <span class="codeph"><span class="varname"> py</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> px</span> </span>, <span class="codeph"><span class="varname"> py</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> x</span>、<span class="varname"> y</span> 値（ピクセル単位）（int） </p></td> 
 </tr> 
</table>

座標 `0,0` は、画像または長方形の左上隅を参照します。 値を大きくすると、右下に向かって移動します。
