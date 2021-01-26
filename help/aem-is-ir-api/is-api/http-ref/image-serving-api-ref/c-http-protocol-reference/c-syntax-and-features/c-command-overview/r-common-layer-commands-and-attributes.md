---
description: これらのコマンドは、画像、テキストおよびべた塗りのレイヤーに適用されます。 ほとんどの要素は、合成画像や単純な非レイヤー要求には意味がありません。 これらは、エフェクトレイヤーには適用されません。
seo-description: これらのコマンドは、画像、テキストおよびべた塗りのレイヤーに適用されます。 ほとんどの要素は、合成画像や単純な非レイヤー要求には意味がありません。 これらは、エフェクトレイヤーには適用されません。
seo-title: 共通のレイヤコマンド
solution: Experience Manager
title: 共通のレイヤコマンド
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f11da6ba-18f2-42d6-8257-cb8ebef8c7d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# 共通画層コマンド{#common-layer-commands}

これらのコマンドは、画像、テキストおよびべた塗りのレイヤーに適用されます。 ほとんどの要素は、合成画像や単純な非レイヤー要求には意味がありません。 これらは、エフェクトレイヤーには適用されません。

<table id="simpletable_8A74E965537D4E8CB91E95AEAE9673E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p> </td> 
  <td class="stentry"> <p>レイヤーの描画モードを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab" type="reference" format="dita" scope="local"> bgColor</a> </p></td> 
  <td class="stentry"> <p>レイヤーの背景色と不透明度を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac" type="reference" format="dita" scope="local"> 延長する</a> </p></td> 
  <td class="stentry"> <p>レイヤーの長方形を拡張（または切り抜き）します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> color</a> </p></td> 
  <td class="stentry"> <p>レイヤーの色と不透明度を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d" type="reference" format="dita" scope="local"> layer</a> </p></td> 
  <td class="stentry"> <p>画層を選択し、z順序を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06" type="reference" format="dita" scope="local"> マップ</a> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップを定義します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>レイヤーの不透明度を下げます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138" type="reference" format="dita" scope="local"> 接触チャネル</a> </p></td> 
  <td class="stentry"> <p>レイヤーの接触チャネル点を設定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>レイヤーをレイヤー0を基準に配置します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-size-reference.md#reference-04d383f32c7b4003bed9978cb854747b" type="reference" format="dita" scope="local"> サイズ</a> </p></td> 
  <td class="stentry"> <p>レイヤサイズコンストレイントを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-hide.md#reference-e336facb21a644eea78c2c84c1c4576e" type="reference" format="dita" scope="local"> 非表示</a> </p></td> 
  <td class="stentry"> <p>レイヤーを非表示にします。 </p></td> 
 </tr> 
</table>

