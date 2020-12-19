---
description: Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、layer=0やlayer=compなど、任意のレイヤー（親レイヤー）にアタッチできる特殊なサブレイヤー（エフェクトレイヤー）を使用して実装されます。
seo-description: Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、layer=0やlayer=compなど、任意のレイヤー（親レイヤー）にアタッチできる特殊なサブレイヤー（エフェクトレイヤー）を使用して実装されます。
seo-title: レイヤー効果
solution: Experience Manager
title: レイヤー効果
topic: Scene7 Image Serving - Image Rendering API
uuid: 076e98de-cbbb-457b-984a-367a935b4356
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 2%

---


# レイヤー効果{#layer-effects}

Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、layer=0やlayer=compなど、任意のレイヤー（親レイヤー）にアタッチできる特殊なサブレイヤー（エフェクトレイヤー）を使用して実装されます。

エフェクトレイヤは、多くの標準的な画像とレイヤ属性およびコマンドをサポートしますが、汎用のレイヤーを想定したものではなく、独立した画像やテキストデータをサポートしません。

1つの親レイヤーに任意の数のレイヤー効果をアタッチできます。

## 内外の効果{#section-2dade7ee98e041d1b4d1725e6f98a515}

*内側の* 効果は親レイヤーの上にレンダリングされ、親レイヤーの不透明な領域にのみ表示されます。*外側の* エフェクトは、親レイヤの後ろにレンダリングされます（したがって、親レイヤの不透明な領域内には表示されません）。また、合成キャンバス内の任意の場所に配置できます。`effect=`コマンドで正または負の効果レイヤー番号を割り当てることで、内側または外側の効果を選択します。 `effect=`コマンドは、同じ親レイヤーにアタッチされた複数のエフェクトレイヤーのz順序も制御します。

## 親レイヤーとの関係{#section-eb8bfc4f754a42fc973b562821d6f2d3}

エフェクトレイヤーは、親レイヤーと一致するように自動的にサイズ設定および配置されます（つまり、エフェクトレイヤーは親レイヤーの`size=`値と`origin=`値を継承します）。 `pos=` は、ドロップ効果とシャドウの内側効果に通常必要なように、エフェクトレイヤーを親レイヤーから離すために使用できます。標準レイヤー`pos=`はこのレイヤーとレイヤー0の接触チャネル間のオフセットを指定しますが、エフェクトレイヤー`pos=`はエフェクトレイヤーと親レイヤーの接触チャネル間のオフセットを指定します。

## サポートされるコマンドと属性{#section-035fc6bcba7d4e7ab4bd46687c1d8879}

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

効果レイヤーに含まれる他の画像およびレイヤーコマンドはすべて無視されます。

## デフォルトのエフェクトマクロ{#section-a01e8dcc87c94495b54a6dfb21d2a718}

レイヤー効果の使用を容易にするために、ISには初期設定の画像カタログ`$shadow$`と`$glow$`の2つのマクロが用意されています。これらのマクロは、Photoshopのレイヤー効果に似たエフェクトレイヤー属性の初期設定値です。 初期設定のレイヤ効果を実装する際に使用する効果コマンドとマクロのリストを、次の表に示します。 当然ながら、マクロで指定されている属性はURLで変更できます。また、カスタムレイヤー効果を実装するために別のマクロを作成することもできます。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 目的の効果</b> </th> 
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

レイヤーに対して50 %追加の不透明度を持つ、幅が3ピクセルの赤い境界線：

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

境界線は、画像のアルファチャネルまたはマスクの輪郭に従います。 `effect=1`を設定すると、境界線が内側の端に配置されます。

初期設定の効果設定（色を除く）を追加使用した、青みがかったドロップシャドウ。

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 画像の右下端に余白を少し追加します。これにより、ドロップシャドウが画像の境界に合わせてクリップされるのを防ぐことができます。

## 関連項目 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [コマンドマクロ%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
