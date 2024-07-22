---
title: 透視図
description: パース変換。 パースペクティブ変換をレイヤーソースイメージに適用して、四角形で指定された領域を埋めます。 レイヤーのその他の領域は透明なままです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 透視図{#perspective}

パース変換。 パースペクティブ変換をレイヤーソースイメージに適用して、四角形で指定された領域を埋めます。 レイヤーのその他の領域は透明なままです。

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>perspQuad を <span class="varname"> 用する </span> </p></td> 
  <td class="stentry"> <p>パースペクティブ四角形のピクセル座標（8 つの実数、コンマで区切る）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>パースペクティブ四辺形の正規化座標（8 つの実数、コンマで区切る）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>再サンプリングオプション（後述）。 </p></td> 
 </tr> 
</table>

モディファイヤ *`perspQuad`* は、合成（またはレイヤ 0）座標空間内の 4 つのピクセル座標値で構成されます。これは、合成イメージの左上コーナーから始まります。

モディファイヤ `perspQuadN` は、4 つの正規化された座標値で構成されます。`0.0,0.0` は、合成/レイヤ 0 イメージの左上コーナーに対応し、右下コーナーに `1.0,1.0` ります。

入力画像は、入力画像の左上隅が `perspQuad[N]` の第 1 座標値に、右上隅が第 2 座標に、右下隅が第 3 座標に、左下隅が第 4 座標にマッピングされるように変換される。

>[!NOTE]
>
>この修飾子 `pos=` を使用すると、合成画像内で変換後のレイヤーをさらに配置できます。

透視四辺形の座標は、合成画像の外側に配置することができる。

四辺形がパース変換に適していない場合、動作は未定義です。 たとえば、2 つ以上の頂点が一致する場合、3 つまたはすべての頂点が同じ線上にある場合、または四角形が自己交差または凹形である場合などです。

## 品質に関する考慮事項 {#section-7cc9056afa614300a9b8844d39739fc3}

デフォルトの実装では、画質とパフォーマンスの間に妥当な妥協点が生成されますが、場合によっては、シャープネスを向上させるためにソースイメージの解像度を上げるか、エイリアシングのアーティファクトを減らすために解像度を下げる必要があります。

ソースが画像の場合は、`scale=` を使用して（画像の最大解像度に対する）別の解像度を選択します。 指定された `scale=` の値は、次に高い PTIF 解像度レベルに丸められます。 ネストされたリクエストソースがある場合は、ネストされたリクエストによって生成される画像のサイズを、必要なシャープネスを達成するように調整できます。 テキストレイヤーの場合、入力イメージ（レンダリングされたテキスト）の解像度は、`textAttr=` で指定された解像度を増やして大きい size=値を選択することで調整されます。

この修飾子 *`resOptions`* を使用すると、別の再サンプリングアルゴリズムを選択できます。 次の値がサポートされています（大文字と小文字が区別されます）。

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 値 </b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> 最寄りの隣人。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 双線形。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 標準スーパーサンプリング （デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> ジッタを調整できるスーパーサンプリング（<span class="varname"> n</span> は、0 ～ 200 の整数値である必要があります）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-818e57df0a1b4449888543bc6af77751}

[ 画層 ] コマンド： 現在の画層、または `layer=comp` の場合は画層 0 に適用されます。 エフェクトレイヤーで無視されます。

同じレイヤーにパースペクティブが存在する場合、修飾子 `res=` は常に無視されます。 画像レイヤーに対して指定した場合、修飾子 `size=` は無視されます。 `perspective=` を含むレイヤー内の修飾子 `size=` と `res=` は、今後の使用のために予約されています。

## 初期設定 {#section-e35683395d514d4eb6b32924e1bf8f2f}

パースペクティブ変換を行わない場合は、`None` を使用します。

## 関連項目 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
