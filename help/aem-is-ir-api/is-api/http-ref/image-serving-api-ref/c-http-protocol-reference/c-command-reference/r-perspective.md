---
title: 視点
description: パースペクティブ変換。 四辺形で指定した領域を塗りつぶすには、レイヤソースイメージにパース変換を適用します。 レイヤーの他の領域は透明のままです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# 視点{#perspective}

パースペクティブ変換。 四辺形で指定した領域を塗りつぶすには、レイヤソースイメージにパース変換を適用します。 レイヤーの他の領域は透明のままです。

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>遠近四辺形のピクセル座標（8 個の実数、コンマ区切り）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>パース四辺形の正規化座標（8 本の実数、コンマ区切り）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>再サンプリングオプション（以下を参照） </p></td> 
 </tr> 
</table>

*`perspQuad`* 合成イメージの左上隅を起点とする合成（またはレイヤ 0）座標空間の 4 つのピクセル座標値で構成されます。

`perspQuadN` は 4 つの正規化された座標値で構成され、 `0.0,0.0` は、合成/レイヤー 0 イメージの左上隅に対応し、 `1.0,1.0` を右下隅に追加します。

入力画像の左上隅がの最初の座標値にマッピングされるように、入力画像が変換されます。 `perspQuad[N]`の場合は、右上隅から 2 番目の座標、右下隅から 3 番目の座標、左下隅から 4 番目の座標です。

>[!NOTE]
>
>`pos=` を使用して、変換後のレイヤーを合成イメージ内にさらに配置することができます。

パースペクティブの四辺形座標は、合成画像の外側に配置される場合があります。

四辺形がパース変換に適さない場合（たとえば、2 つ以上の頂点が一致する場合、3 つ以上の頂点が同じ線上にある場合、または四辺形が自己交差または凹面の場合）は、動作は未定義です。

## 品質に関する考慮事項 {#section-7cc9056afa614300a9b8844d39739fc3}

デフォルトの実装では、画質とパフォーマンスの間に妥当な妥協が生じますが、場合によっては、ソース画像の解像度を上げてシャープネスを改善したり、エイリアシングアーティファクトを減らしたりする必要があります。

ソースが画像の場合は、 `scale=` をクリックして、（画像の最大解像度を基準に）別の解像度を選択します。 指定した `scale=` の値は、次に高い PTIF 解像度レベルに丸められます。 リクエストソースがネストされている場合は、ネストされたリクエストで生成される画像のサイズを調整して、希望のシャープネスを実現できます。 テキストレイヤーの場合、入力画像（レンダリングされたテキスト）の解像度は、で指定した解像度を増やすと共に大きい size=値を選択することで調整されます。 `textAttr=`.

*`resOptions`* では、別の再サンプリングアルゴリズムを選択できます。 次の値がサポートされます（大文字と小文字が区別されます）。

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
   <td> <p> バイリニア法。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 標準のスーパーサンプリング（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 調整可能なジッタ (<span class="varname"> n</span> は、0 ～ 200 の整数値である必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-818e57df0a1b4449888543bc6af77751}

[ 画層 ] コマンド 現在の画層に適用されます。 `layer=comp`. 効果画層で無視されます。

`res=` は、同じレイヤにパースペクティブが存在する場合は常に無視されます。 `size=` は、画像レイヤに対して指定された場合は無視されます。 `size=` および `res=` 次のレイヤーで `perspective=` は将来の使用のために予約されています。

## 初期設定 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`（透視投影変換なし）。

## 関連項目 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
