---
description: 正規化座標。 画像内の相対位置（画像オフセットや切り抜きパラメータなど）を、画像のサイズに合わせて正規化するために使用します。
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# coordN{#coordn}

正規化座標。 画像内の相対位置（画像オフセットや切り抜きパラメータなど）を、画像のサイズに合わせて正規化するために使用します。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>画像のサイズに正規化された座標オフセット（実数、実数） </p></td> 
 </tr> 
</table>

正の値は右下に移動します。

多くの場合、参照位置が画像の中心になります。 この場合、0,0は画像の中心、-0.5、-0.5は左上隅、0.5,0.5は右下隅に対応します。

また、レイヤー0のサイズを基準にして、画像サイズまたは長方形サイズを指定する場合にも使用します。 この場合、値は0より大きい値にする必要があります。 0は、特定のデフォルト値を使用する必要があることを示します。 1,1はレイヤ0と等しいサイズを指定します。
