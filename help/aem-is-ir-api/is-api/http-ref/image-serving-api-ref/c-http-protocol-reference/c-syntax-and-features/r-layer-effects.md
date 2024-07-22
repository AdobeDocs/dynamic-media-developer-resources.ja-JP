---
title: レイヤー効果
description: Photoshopスタイルのレイヤーシャドウおよびグロー効果は、特別なサブレイヤー（エフェクトレイヤー）を使用して実装され、レイヤー=0 やレイヤー=comp など、任意のレイヤー（親レイヤー）にアタッチできます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---

# レイヤー効果{#layer-effects}

Photoshopスタイルのレイヤーシャドウおよびグロー効果は、特別なサブレイヤー（エフェクトレイヤー）を使用して実装され、レイヤー=0 やレイヤー=comp など、任意のレイヤー（親レイヤー）にアタッチできます。

エフェクトレイヤーは、多数の標準の画像およびレイヤーの属性とコマンドをサポートしていますが、汎用的なレイヤーではなく、独立した画像やテキストデータをサポートしていません。

1 つの親レイヤーに任意の数のレイヤー効果をアタッチできます。

## 内側と外側のエフェクト {#section-2dade7ee98e041d1b4d1725e6f98a515}

*内部効果* は親レイヤーの上にレンダリングされ、親レイヤーの不透明領域にのみ表示されます。 *外部エフェクト* は親レイヤーの背後にレンダリングされるため、親レイヤーの不透明な領域には表示されません。合成キャンバス内のどこにでも配置できます。 内側または外側の効果は、`effect=` コマンドでプラスまたはマイナスの効果レイヤー番号を割り当てることによって選択されます。 `effect=` のコマンドは、同じ親レイヤーにアタッチされた複数のエフェクトレイヤー間の z 順序も制御します。

## 親レイヤーとの関係 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

エフェクトレイヤーは、親レイヤーと一致するように自動的にサイズが調整されて配置されます（つまり、エフェクトレイヤーは親レイヤーの `size=` と `origin=` の値を継承します）。 ドロップエフェクト `pos=` シャドウの内側エフェクトで通常必要とされるように、エフェクトレイヤーを親レイヤーから遠ざける場合に使用できます。 標準レイヤーの場合は `pos=` このレイヤーの起点とレイヤー 0 との間のオフセットを指定し、エフェクトレイヤーの場合は `pos=` エフェクトレイヤーの起点と親レイヤーとの間のオフセットを指定します。

## サポートされるコマンドと属性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

エフェクトレイヤーでは、以下のコマンドと属性を使用できます。

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

エフェクトレイヤーに含まれているその他の画像コマンドやレイヤーコマンドは無視されます。

## デフォルトのエフェクトマクロ {#section-a01e8dcc87c94495b54a6dfb21d2a718}

レイヤー効果の使用を容易にするために、IS にはデフォルトの画像カタログである `$shadow$` と `$glow$` を備えた 2 つのマクロが用意されています。これらのマクロは、Photoshop レイヤー効果に似たエフェクトレイヤー属性のデフォルト値を提供します。 次の表に、既定のレイヤー効果を実装するために使用する効果コマンドとマクロを示します。 当然、マクロで指定された属性は URL で変更したり、代替マクロを作成してカスタムのレイヤー効果を実装したりできます。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 望ましい効果 </b> </th> 
   <th class="entry"> <b> コマンド </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> ドロップシャドウ </p> </td> 
   <td> <p> <span class="codeph"> 効果=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> シャドウ（内側） </p> </td> 
   <td> <p> <span class="codeph"> 効果=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 光彩（外側） </p> </td> 
   <td> <p> <span class="codeph"> 効果=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 光彩（内側） </p> </td> 
   <td> <p> <span class="codeph"> 効果=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-4c449fdf707b43858917fb271fa1fe96}

次のように、不透明度 50% の 3 ピクセル幅の赤い境界線をレイヤーに追加します。

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

境界線は、イメージのアルファ チャンネルまたはマスクの輪郭に従います。 `effect=1` を設定すると、代わりに内側のエッジに境界が配置されます。

デフォルトの効果設定（カラーを除く）を使用して、画像に青みがかったドロップシャドウを追加します。

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` では、画像の右下のエッジに少し余白が追加されるので、ドロップシャドウが画像の境界にクリッピングされるのを防ぐことができます。

## 関連項目 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [ コマンド マクロ %l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
