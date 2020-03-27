---
description: Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、特別なサブレイヤー（エフェクトレイヤー）を使用して実装されます。このサブレイヤーは、layer=0やlayer=compなど、任意のレイヤー（親レイヤー）にアタッチできます。
seo-description: Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、特別なサブレイヤー（エフェクトレイヤー）を使用して実装されます。このサブレイヤーは、layer=0やlayer=compなど、任意のレイヤー（親レイヤー）にアタッチできます。
seo-title: レイヤー効果
solution: Experience Manager
title: レイヤー効果
topic: Scene7 Image Serving - Image Rendering API
uuid: 076e98de-cbbb-457b-984a-367a935b4356
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# レイヤー効果{#layer-effects}

Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、特別なサブレイヤー（エフェクトレイヤー）を使用して実装されます。このサブレイヤーは、layer=0やlayer=compなど、任意のレイヤー（親レイヤー）にアタッチできます。

エフェクトレイヤーは、多くの標準的な画像とレイヤーの属性とコマンドをサポートしていますが、汎用のレイヤーを想定しておらず、独立した画像やテキストデータをサポートしていません。

1つの親レイヤーに任意の数のレイヤー効果をアタッチできます。

## 内外の効果 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*内部効果は* 、親レイヤーの上にレンダリングされ、親レイヤーの不透明な領域にのみ表示されます。 *外側のエフェクトは* 、親レイヤの後ろにレンダリングされ（親レイヤの不透明な領域内には表示されない）、合成キャンバス内の任意の場所に配置できます。 内側または外側の効果は、コマンドで正または負の効果のレイヤー番号を割り当てることで選択 `effect=` します。 同じ親レ `effect=` イヤーにアタッチされた複数のエフェクトレイヤー間のz順序も制御します。

## 親レイヤーとの関係 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

エフェクトレイヤーは、親レイヤーと同時にサイズ設定され、配置されます(つまり、エフェクトレイヤーは親レ `size=` イヤーの `origin=` 値と値を継承します)。 `pos=` は、ドロップシャドウ効果やシャドウ（内側）効果の場合に通常必要なように、エフェクトレイヤーを親レイヤーから離すために使用します。 標準レイヤーでは、こ `pos=` のレイヤーの原点とレイヤー0の間のオフセットを指定しますが、エフェクトレイヤーでは、エ `pos=` フェクトレイヤーと親レイヤーの原点間のオフセットを指定します。

## サポートされるコマンドと属性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

エフェクトレイヤーには、次のコマンドと属性を使用できます。

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

エフェクトレイヤーに含まれる他の画像およびレイヤーコマンドはすべて無視されます。

## デフォルトのエフェクトマクロ {#section-a01e8dcc87c94495b54a6dfb21d2a718}

ISでは、レイヤー効果を使用しやすくするために、初期設定の画像カタログと共に2つのマクロが用意されています。また、ISは、Photoshopのレイヤー効果に類似したエフェクトレイヤー `$shadow$``$glow$`属性の初期設定値を提供します。 次の表に、初期設定のレイヤー効果を実装するために使用する効果コマンドとマクロを示します。 マクロで指定した属性は、URLで変更することも、カスタムレイヤー効果を実装する別のマクロを作成することもできます。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 望ましい効果</b> </th> 
   <th class="entry"> <b> コマンド</b> </th> 
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
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 光彩（内側） </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-4c449fdf707b43858917fb271fa1fe96}

レイヤーに、不透明度50 %の幅が3ピクセルの赤い境界線を追加します。

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

境界線は、画像のアルファチャンネルまたはマスクの輪郭に従います。 この設 `effect=1` 定により、境界線が内側の境界線に配置されます。

初期設定の効果設定（色を除く）を使用して、青みがかったドロップシャドウを画像に追加します。

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 画像の右下端に少しのマージンを追加します。これにより、ドロップシャドウが画像の境界に沿ってクリップされるのを防ぎます。

## 関連項目 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Command Macros%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
