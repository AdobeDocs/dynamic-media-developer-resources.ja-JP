---
title: coordN
description: 正規化された座標。 画像内の相対位置を指定するために使用します。例えば、画像のサイズに合わせて正規化された画像オフセットや切り抜きパラメータなどです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# coordN{#coordn}

正規化された座標。 画像内の相対位置を指定するために使用します。例えば、画像のサイズに合わせて正規化された画像オフセットや切り抜きパラメータなどです。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>画像のサイズに合わせて正規化された座標オフセット（実数、実数） </p></td> 
 </tr> 
</table>

正の値は右下に向かって移動します。

多くの場合、参照位置は画像の中心です。 この場合、 `0,0` は、画像の中央に対応します。 `-0.5,-0.5` を左上隅に、 `0.5,0.5` を右下隅に追加します。

また、レイヤー 0 のサイズを基準に画像サイズまたは長方形サイズを指定する場合にも使用します。 この場合、値は 0 より大きい値にする必要があります。 0 は、特定のデフォルト値を使用する必要があることを示す場合があります。 値： `1,1` は、レイヤ 0 と等しいサイズを指定します。
