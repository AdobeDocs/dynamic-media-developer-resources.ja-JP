---
title: レイヤー効果
description: Photoshopスタイルのレイヤーシャドウとグロー効果は、layer=0やlayer=compを含む任意のレイヤー（親レイヤー）にアタッチできる特殊なサブレイヤー（エフェクトレイヤー）を使用して実装されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
TQID: 'https://experienceleague.adobe.com/q8tty512IzvWyTXbv2l31DSuqOnijcyhwITruFv7zS0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 494
ht-degree: 2%

---

# レイヤー効果{#layer-effects}

Photoshopスタイルのレイヤーシャドウとグロー効果は、layer=0やlayer=compを含む任意のレイヤー（親レイヤー）にアタッチできる特殊なサブレイヤー（エフェクトレイヤー）を使用して実装されます。

エフェクトレイヤーは、多くの標準的な画像およびレイヤー属性とコマンドをサポートしていますが、一般的なレイヤーを意図したものではなく、独立した画像データやテキストデータをサポートしていません。

1つの親レイヤーには、任意の数のレイヤー効果をアタッチできます。

## インナーエフェクトとアウターエフェクト {#section-2dade7ee98e041d1b4d1725e6f98a515}

*インナーエフェクト*&#x200B;は親レイヤーの上にレンダリングされ、親レイヤーの不透明部分でのみ表示されます。 *外部効果*&#x200B;は、親レイヤーの後ろにレンダリングされます（したがって、親レイヤーの不透明領域内には表示されません）。合成キャンバス内のどこにでも配置できます。 内側または外側のエフェクトは、`effect=` コマンドで正または負のエフェクトレイヤー番号を割り当てることで選択します。 また、`effect=` コマンドは、同じ親レイヤーにアタッチされた複数のエフェクトレイヤー間のz順序も制御します。

## 親レイヤーとの関係 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

エフェクトレイヤーは、親レイヤーと一致するように自動的にサイズ調整および配置されます（つまり、エフェクトレイヤーは親レイヤーの`size=`と`origin=`の値を継承します）。 `pos=`を使用すると、通常はドロップシャドウ効果とシャドウ効果の内側に必要なように、エフェクトレイヤーを親レイヤーから離すことができます。 標準レイヤー`pos=`の場合は、このレイヤーの原点とレイヤー0の間のオフセットを指定しますが、エフェクトレイヤー`pos=`の場合は、エフェクトレイヤーの原点と親レイヤーの間のオフセットを指定します。

## サポートされているコマンドと属性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

エフェクトレイヤーでは、次のコマンドと属性を使用できます。

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

エフェクトレイヤーに含まれている他のすべての画像コマンドとレイヤーコマンドは無視されます。

## デフォルトのエフェクトマクロ {#section-a01e8dcc87c94495b54a6dfb21d2a718}

レイヤーエフェクトの使用を容易にするために、ISは、Photoshop レイヤーエフェクトに似たエフェクトレイヤー属性のデフォルト値を提供するデフォルトの画像カタログ `$shadow$`と`$glow$`を備えた2つのマクロを提供します。 次の表に、デフォルトのレイヤー効果を実装するために使用するエフェクトコマンドとマクロを示します。 当然のことながら、マクロで指定された属性はすべてURLで変更できるか、代替マクロを作成してカスタムレイヤー効果を実装できます。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>望ましい効果</b> </th> 
   <th class="entry"> <b> コマンド </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> ドロップシャドウ </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> シャドウ（内側） </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 光彩（外側） </p> </td> 
   <td> <p> <span class="codeph">効果=-1&amp;$光彩$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 光彩（内側） </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-4c449fdf707b43858917fb271fa1fe96}

レイヤーに不透明度50%の幅の3 ピクセルの赤い境界線を追加します。

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

境界線は、画像のアルファチャンネルまたはマスクの輪郭に従います。 `effect=1`を設定すると、代わりに境界線が内側のエッジに配置されます。

デフォルトのエフェクト設定（カラーを除く）を使用して、画像に青みのあるドロップシャドウを追加します。

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=`では、画像の右下の端にマージンが少し追加され、ドロップシャドウが画像の境界にクリップされなくなります。

## 関連項目 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [ コマンドマクロ %l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
