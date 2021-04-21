---
description: 正規化座標。 画像のサイズに合わせて標準化された、画像のオフセットや切り抜きパラメータなど、画像内の相対位置を指定するために使用します。
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# coordN{#coordn}

正規化座標。 画像のサイズに合わせて標準化された、画像のオフセットや切り抜きパラメータなど、画像内の相対位置を指定するために使用します。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>画像のサイズに合わせて正規化された座標オフセット(real, real) </p></td> 
 </tr> 
</table>

正の値は右下に向かって移動します。

多くの場合、参照位置が画像の中心です。 この場合、0,0は画像の中心に対応し、-0.5、-0.5は左上隅、0.5,0.5は右下隅に対応します。

また、レイヤー0のサイズを基準にして、画像サイズまたは長方形サイズを指定する場合にも使用します。 この場合、0より大きい値を指定する必要があります。 0の場合は、特定のデフォルト値を使用する必要があります。 1,1は、レイヤ0と同じサイズを指定します。
