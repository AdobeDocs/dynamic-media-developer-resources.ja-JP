---
description: これらのコマンドは、画像、テキストおよび単色レイヤーに適用されます。 そのほとんどは、合成画像やシンプルでレイヤー化されていない要求には意味がありません。 エフェクトレイヤーには適用されません。
solution: Experience Manager
title: 一般的なレイヤーコマンド
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c95d198c-757f-405e-ba08-094cd402c929
TQID: 'https://experienceleague.adobe.com/G0cmUcGA4L4g1-pfGgi0mZvr3macOhjkUfQPQ9ifQkg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 140
ht-degree: 0%

---

# 一般的なレイヤーコマンド{#common-layer-commands}

これらのコマンドは、画像、テキストおよび単色レイヤーに適用されます。 そのほとんどは、合成画像やシンプルでレイヤー化されていない要求には意味がありません。 エフェクトレイヤーには適用されません。

<table id="simpletable_8A74E965537D4E8CB91E95AEAE9673E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p> </td> 
  <td class="stentry"> <p>レイヤー描画モードを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab" type="reference" format="dita" scope="local"> bgColor</a> </p></td> 
  <td class="stentry"> <p>レイヤーの背景色と不透明度を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac" type="reference" format="dita" scope="local"> extend</a> </p></td> 
  <td class="stentry"> <p>レイヤーの長方形を拡張（または切り抜き）します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> カラー</a> </p></td> 
  <td class="stentry"> <p>レイヤーのカラーと不透明度を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d" type="reference" format="dita" scope="local"> レイヤー</a> </p></td> 
  <td class="stentry"> <p>レイヤーを選択し、Z次を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06" type="reference" format="dita" scope="local"> マップ </a> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップを定義します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>レイヤーの不透明度を下げます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138" type="reference" format="dita" scope="local"> オリジン </a> </p></td> 
  <td class="stentry"> <p>レイヤーの原点を設定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>レイヤーをレイヤー0に相対的に配置します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-size-reference.md#reference-04d383f32c7b4003bed9978cb854747b" type="reference" format="dita" scope="local"> サイズ </a> </p></td> 
  <td class="stentry"> <p>レイヤーサイズの制約を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-hide.md#reference-e336facb21a644eea78c2c84c1c4576e" type="reference" format="dita" scope="local">非表示</a> </p></td> 
  <td class="stentry"> <p>レイヤーを非表示にします。 </p></td> 
 </tr> 
</table>
