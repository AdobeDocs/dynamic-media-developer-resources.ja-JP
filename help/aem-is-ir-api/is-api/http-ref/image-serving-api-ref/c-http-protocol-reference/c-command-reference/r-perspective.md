---
description: パース変換。 四辺形で指定した領域を塗りつぶすには、レイヤソースイメージにパース変換を適用します。 レイヤーのその他の領域は透明のままです。
solution: Experience Manager
title: 視点
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# 視点{#perspective}

パース変換。 四辺形で指定した領域を塗りつぶすには、レイヤソースイメージにパース変換を適用します。 レイヤーのその他の領域は透明のままです。

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>パース四辺形のピクセル座標（コンマ区切りの8個の実数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>パース四辺形の正規化座標（コンマ区切りの8個の実数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>再サンプリングオプション（以下を参照） </p></td> 
 </tr> 
</table>

*`perspQuad`* は、合成画像の左上隅を起点とする合成（またはレイヤ0）座標空間の4つのピクセル座標値で構成されます。

`perspQuadN` は、4つの正規化された座標値で構成さ `0.0,0.0` れます。ここでは、コンポジット/レイヤー0画像の左上隅と右下隅 `1.0,1.0` に対応します。

入力画像の左上隅が第1の座標値`perspQuad[N]`に、右上隅が第2の座標に、右下隅が第3の座標に、左下隅が第4の座標にマッピングされるように、入力画像が変換される。

>[!NOTE]
>
>`pos=` を使用して、コンポジットイメージ内で変換後のレイヤーをさらに配置することができます。

パースペクティブの四辺形座標は、合成画像の外側に位置する場合があります。

四辺形がパース変換に適していない場合（たとえば、2つ以上の頂点が一致する場合、3つ以上の頂点が同じ線上にある場合、または四辺形が自己交差または凹面の場合）、動作は定義されません。

## 品質に関する考慮事項 {#section-7cc9056afa614300a9b8844d39739fc3}

デフォルトの実装では、画質とパフォーマンスの間に妥当な妥協点が生じますが、場合によっては、ソース画像の解像度を高めてシャープネスを改善したり、エイリアシングアーティファクトを減らしたりする必要があります。

ソースが画像の場合は、`scale=`を使用して（画像の最大解像度を基準に）異なる解像度を選択します。 指定された`scale=`値は、次に高いPTIF解像度レベルに丸められます。 ネストされたリクエストソースの場合、ネストされたリクエストによって生成される画像のサイズを調整して、所望のシャープネスを実現できます。 テキストレイヤーの場合、`textAttr=`で指定される解像度を増やすことに伴い、より大きなsize=値を選択することで、入力画像（レンダリングされたテキスト）の解像度を調整します。

*`resOptions`* では、別の再サンプリングアルゴリズムを選択できます。次の値がサポートされています（大文字と小文字が区別されます）。

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
   <td> <p> 標準のスーパーサンプリング（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> 調整可能なジッター（<span class="varname"> n</span>は0 ～ 200の整数値）を持つスーパーサンプリング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-818e57df0a1b4449888543bc6af77751}

レイヤコマンド 現在の画層に適用され、 `layer=comp`の場合は画層0に適用されます。 エフェクトレイヤでは無視されます。

`res=` は、同じレイヤにパースペクティブが存在する場合は常に無視されます。`size=` は、イメージレイヤに対して指定された場合は無視されます。`size=` とを含 `res=` むレイヤー `perspective=` は、今後の使用のために予約されています。

## 初期設定 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`（透視投影変換なし）。

## 関連項目 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) 、 [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)、 [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)、 [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
