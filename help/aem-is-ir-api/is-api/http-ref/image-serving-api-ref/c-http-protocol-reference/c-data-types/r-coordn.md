---
description: 正規化座標。 画像のサイズに合わせて標準化された、画像のオフセットや切り抜きパラメータなど、画像内の相対位置を指定するために使用します。
seo-description: 正規化座標。 画像のサイズに合わせて標準化された、画像のオフセットや切り抜きパラメータなど、画像内の相対位置を指定するために使用します。
seo-title: coordN
solution: Experience Manager
title: coordN
topic: Scene7 Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# coordN{#coordn}

正規化座標。 画像のサイズに合わせて標準化された、画像のオフセットや切り抜きパラメータなど、画像内の相対位置を指定するために使用します。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> , ny </span><span class="codeph"><span class="varname"></span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> , ny </span><span class="codeph"><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>画像のサイズに正規化された座標オフセット（実数、実数） </p></td> 
 </tr> 
</table>

正の値は右下に向かって移動します。

多くの場合、参照位置が画像の中心です。 この場合、0,0は画像の中心に対応し、-0.5、-0.5は左上隅に、0.5,0.5は右下隅に対応します。

また、レイヤー0のサイズを基準にした画像サイズや長方形サイズの指定にも使用します。 この場合、値は0より大きい必要があります。 0は、特定のデフォルト値を使用することを示します。 1,1は、レイヤー0と同じサイズを指定します。
