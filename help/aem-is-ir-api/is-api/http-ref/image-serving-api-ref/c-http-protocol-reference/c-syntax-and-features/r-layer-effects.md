---
title: レイヤー効果
description: Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、layer=0 や layer=comp など、任意のレイヤー（親レイヤー）にアタッチできる特殊なサブレイヤー（エフェクトレイヤー）を使用して実装されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 2%

---

# レイヤー効果{#layer-effects}

Photoshopスタイルのレイヤーシャドウ効果と光彩効果は、layer=0 や layer=comp など、任意のレイヤー（親レイヤー）にアタッチできる特殊なサブレイヤー（エフェクトレイヤー）を使用して実装されます。

エフェクトレイヤは、多くの標準的なイメージとレイヤの属性とコマンドをサポートしますが、汎用のレイヤではなく、独立したイメージやテキストデータをサポートしません。

1 つの親レイヤーに任意の数のレイヤー効果をアタッチできます。

## 内外の効果 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*内側の効果* は親レイヤーの上にレンダリングされ、親レイヤーの不透明な領域にのみ表示されます。 *外側の効果* は親レイヤの後ろにレンダリングされます（親レイヤの不透明な領域内には表示されません）。また、合成キャンバス内の任意の場所に配置できます。 内側または外側の効果は、正または負の効果レイヤー番号を `effect=` コマンドを使用します。 この `effect=` コマンドは、同じ親レイヤーにアタッチされた複数のエフェクトレイヤーの z 順序も制御します。

## 親レイヤーとの関係 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

エフェクトレイヤーは、親レイヤーと一致するように、自動的にサイズが調整され、配置されます ( つまり、エフェクトレイヤーは `size=` および `origin=` 親レイヤーの値 )。 `pos=` は、ドロップ効果や内側のシャドウ効果に通常必要とされるように、エフェクトレイヤーを親レイヤーから離すために使用できます。 標準レイヤーの場合 `pos=` このレイヤーの原点とレイヤー 0 の間のオフセットを指定します（エフェクトレイヤーの場合）。 `pos=` 効果レイヤーの原点と親レイヤーの間のオフセットを指定します。

## サポートされるコマンドと属性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

エフェクトレイヤは、次のコマンドと属性を受け付けます。

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

エフェクトレイヤに含まれる他のイメージコマンドとレイヤコマンドは無視されます。

## デフォルト効果マクロ {#section-a01e8dcc87c94495b54a6dfb21d2a718}

IS では、レイヤ効果の使用を容易にするために、既定のイメージカタログを使用して 2 つのマクロを提供しています。 `$shadow$` および `$glow$`:Photoshopのレイヤー効果に似た効果レイヤー属性のデフォルト値を提供します。 次の表に、既定のレイヤ効果の実装に使用する効果コマンドとマクロを示します。 当然ながら、マクロで指定された属性は URL 内で修正することも、カスタムレイヤー効果を実装する代替マクロを作成することもできます。

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

レイヤーに、不透明度 50%の 3 ピクセル幅の赤い境界線を追加します。

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

境界線は、画像のアルファチャンネルまたはマスクの輪郭に従います。 設定 `effect=1` 境界線を内側の端に配置します。

初期設定の効果設定（色を除く）を使用して、画像に青いドロップシャドウを追加します。

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 画像の右下端に小さな余白を追加します。これにより、ドロップシャドウが画像の境界にクリップされるのを防ぎます。

## 関連項目 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [コマンドマクロ%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
