---
description: 遠近法の変換 四辺形で指定した領域を塗りつぶすには、遠近法の変換をレイヤーのソース画像に適用します。 レイヤーの他の領域は透明のままです。
seo-description: 遠近法の変換 四辺形で指定した領域を塗りつぶすには、遠近法の変換をレイヤーのソース画像に適用します。 レイヤーの他の領域は透明のままです。
seo-title: 視点
solution: Experience Manager
title: 視点
topic: Scene7 Image Serving - Image Rendering API
uuid: b22d7b49-db08-48df-80bc-5b7237aea475
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 視点{#perspective}

遠近法の変換 四辺形で指定した領域を塗りつぶすには、遠近法の変換をレイヤーのソース画像に適用します。 レイヤーの他の領域は透明のままです。

`perspective= *`perspQuadresOptions`*[, *``*]`

`perspectiveN= *`perspQuadNresOptions`*[, *``*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>遠近の四辺形のピクセル座標（8個の実数、コンマで区切る）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>遠近法の四辺形の正規化座標（8個の実数、コンマで区切る）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>再サンプルオプション（以下を参照） </p></td> 
 </tr> 
</table>

*`perspQuad`* は、合成イメージの左上隅を起点とする合成（またはレイヤー0）座標空間の4つのピクセル座標値で構成されます。

`perspQuadN` は、4つの正規化された座標値で構成さ `0.0,0.0` れます。この座標値は、合成/レイヤー0画像の左上隅と `1.0,1.0` 右下隅に対応します。

入力画像の左上隅がの第1の座標値、右上隅が第2の座標、右下隅が第3の座標、左下隅が第4の座標に対応するように、入力画像が変換されます。 `perspQuad[N]`

>[!NOTE]
>
>`pos=` を使用して、合成画像内の変換後のレイヤーをさらに配置できます。

遠近の四辺形座標は、合成画像の外側に配置できます。

四辺形が遠近法の変換に適していない場合（たとえば、2つ以上の頂点が一致する場合、3つ以上の頂点が同じ線上にある場合、または四辺形が自己交差または凹面の場合）、動作は未定義です。

## 品質に関する考慮事項 {#section-7cc9056afa614300a9b8844d39739fc3}

デフォルトの実装では品質とパフォーマンスの間に妥当な違いが生じますが、場合によっては、ソース画像の解像度を高めてシャープを向上させたり、エイリアシングアーチファクトを減らしたりする必要があります。

ソースが画像の場合は、を使用し `scale=` て、画像の最大解像度を基準とする別の解像度を選択します。 指定した値 `scale=` は、次に高いPTIF解像度レベルに丸められます。 ネストされたリクエストソースの場合は、ネストされたリクエストで生成される画像のサイズを調整して、希望のシャープを実現できます。 テキストレイヤーの場合、で指定した解像度を増やすと共に、大きいsize=値を選択して、入力画像（レンダリングされたテキスト）の解像度を調整しま `textAttr=`す。

*`resOptions`* 別の再サンプルアルゴリズムを選択できます。 次の値がサポートされています（大文字と小文字が区別されます）。

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 値</b> </th> 
   <th class="entry"> <b> 説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> 最も近い隣人。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> バイリニア法. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 標準スーパーサンプリング（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 調整可能なジッターを持つスーパーサンプリ<span class="varname"> ング(</span> nは0 ～ 200の整数値である必要があります)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-818e57df0a1b4449888543bc6af77751}

レイヤーコマンド 現在のレイヤに適用されます。レイヤ0の場合は適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

`res=` は、同じレイヤーにパースペクティブが存在する場合は常に無視されます。 `size=` は、画像レイヤーに対して指定した場合は無視されます。 `size=` との重 `res=` なりは、今後の使 `perspective=` 用のために予約されています。

## 初期設定 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`（遠近法の変換なし）。

## 関連項目 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
