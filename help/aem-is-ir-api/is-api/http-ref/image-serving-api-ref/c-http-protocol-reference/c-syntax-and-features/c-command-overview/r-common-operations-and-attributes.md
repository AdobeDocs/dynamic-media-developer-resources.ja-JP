---
description: これらのコマンドは、画像、テキスト、および単色のレイヤーに適用されます。 また、通常は、合成画像や、シンプルな非レイヤー画像リクエストにも役立ちます。
solution: Experience Manager
title: 一般的な操作
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f30a9653-7aed-4233-8361-18ca6561d420
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 一般的な操作{#common-operations}

これらのコマンドは、画像、テキスト、および単色のレイヤーに適用されます。 また、通常は、合成画像や、シンプルな非レイヤー画像リクエストにも役立ちます。

<table id="simpletable_996969D618C94BE8B81FAED512B5B7BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>レイヤをぼかします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a" type="reference" format="dita" scope="local"> op_brightness</a> </p></td> 
  <td class="stentry"> <p>レイヤーの明るさを調整します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-colorbalance.md#reference-fb6af4ecf0f842d3adfdda342834a8fd" type="reference" format="dita" scope="local"> op_colorbalance</a> </p></td> 
  <td class="stentry"> <p>赤、緑、青を個別に調整します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> op_colorize</a> を <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-colorize.md#reference-50399231d6dc4c15b3ab5b93c32c458a" type="reference" format="dita" scope="local"> します </p></td> 
  <td class="stentry"> <p>画層データを色付けします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d" type="reference" format="dita" scope="local"> op_contrast</a> </p></td> 
  <td class="stentry"> <p>コントラストを調整します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-hue.md#reference-4d97f5e206114db8b09132fd6e55ec00" type="reference" format="dita" scope="local"> op_hue</a> </p></td> 
  <td class="stentry"> <p>すべてのカラーの色相をシフトします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-invert.md#reference-5e3a8e9882a74a52acfd503cd7987828" type="reference" format="dita" scope="local"> op_invert</a> </p></td> 
  <td class="stentry"> <p>色を反転します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_noise</a> </p></td> 
  <td class="stentry"> <p>レイヤーにノイズを追加します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-saturation.md#reference-6b7ee05a462f4f01b1fb7108230d90d9" type="reference" format="dita" scope="local"> op_saturation</a> </p></td> 
  <td class="stentry"> <p>カラーの彩度を調整します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541" type="reference" format="dita" scope="local"> op_sharpen</a> </p></td> 
  <td class="stentry"> <p>シンプルなシャープニングを適用します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm</a> </p></td> 
  <td class="stentry"> <p>アンシャープマスクを適用します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> 反転 <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-flip.md#reference-f8568a61b77c41569d382a3147964ce3" type="reference" format="dita" scope="local"> る </a> </p></td> 
  <td class="stentry"> <p>レイヤーを水平方向または垂直方向に反転します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096" type="reference" format="dita" scope="local"> 回転 </a> </p></td> 
  <td class="stentry"> <p>レイヤーを回転します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-perspective.md#reference-c941f3bb1eee4dd29abf3824c0b0bc8e" type="reference" format="dita" scope="local"> perspective</a> </p></td> 
  <td class="stentry"> <p>パースペクティブ – レイヤを変換します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d" type="reference" format="dita" scope="local">clipPath</a> </p></td> 
  <td class="stentry"> <p>レイヤーのクリップ形状を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> clipXPath</a> を <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53" type="reference" format="dita" scope="local"> します </p></td> 
  <td class="stentry"> <p>レイヤーの反転したクリップシェイプを指定します。 </p></td> 
 </tr> 
</table>
