---
description: これらのコマンドを使用して、ドロップシャドウ効果や光彩効果などのレイヤー効果を定義できます。 エフェクトレイヤーは、他のすべてのコマンドを無視します。
seo-description: これらのコマンドを使用して、ドロップシャドウ効果や光彩効果などのレイヤー効果を定義できます。 エフェクトレイヤーは、他のすべてのコマンドを無視します。
seo-title: レイヤー効果コマンド
solution: Experience Manager
title: レイヤー効果コマンド
topic: Scene7 Image Serving - Image Rendering API
uuid: 5fef90d1-0507-497b-9187-869672996852
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# レイヤー効果コマンド{#layer-effect-commands}

これらのコマンドを使用して、ドロップシャドウ効果や光彩効果などのレイヤー効果を定義できます。 エフェクトレイヤーは、他のすべてのコマンドを無視します。

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p></td> 
  <td class="stentry"> <p>レイヤーの描画モードを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> color</a> </p></td> 
  <td class="stentry"> <p>主な効果のカラーと不透明度を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> 効果</a> </p></td> 
  <td class="stentry"> <p>エフェクトレイヤーセグメントを開始し、z順序を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> maskUse</a> </p></td> 
  <td class="stentry"> <p>親のレイヤマスク（アルファチャンネル）の使用方法を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>効果を羽毛で描きます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_grow</a> </p></td> 
  <td class="stentry"> <p>レイヤー効果を拡大または縮小します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_noise</a> </p></td> 
  <td class="stentry"> <p>効果にノイズを追加します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>レイヤーの不透明度を下げます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>親レイヤーを基準にして、エフェクトレイヤーを配置します。 </p></td> 
 </tr> 
</table>
