---
title: 遠近法
description: 遠近法の変換： レイヤーソース画像に遠近法トランスフォームを適用して、四角形で指定された領域を塗りつぶします。 レイヤーの他の領域は透明のままです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
TQID: 'https://experienceleague.adobe.com/XfQCa-7NeORdGGLEc247lv-HQb99vuDE-31hmMuUUGM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# 遠近法{#perspective}

遠近法の変換： レイヤーソース画像に遠近法トランスフォームを適用して、四角形で指定された領域を塗りつぶします。 レイヤーの他の領域は透明のままです。

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>遠近法の四角形ピクセル座標（8実数、コンマで区切る）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>遠近四辺正規化座標（8実数、コンマで区切る）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>リサンプリングオプション（以下を参照）。 </p></td> 
 </tr> 
</table>

修飾子&#x200B;*`perspQuad`*&#x200B;は、合成画像の左上隅に位置する合成座標（またはレイヤー0）空間の4つのピクセル座標値で構成されます。

修飾子`perspQuadN`は4つの正規化された座標値で構成され、`0.0,0.0`は合成/レイヤー0画像の左上隅に対応し、`1.0,1.0`は右下隅に対応します。

入力画像は、入力画像の左上隅が第1座標値`perspQuad[N]`、右上隅が第2座標、右下隅が第3座標、左下隅が第4座標となるように変形される。

>[!NOTE]
>
>修飾子`pos=`を使用すると、変換後のレイヤーを合成画像内でさらに配置できます。

遠近法の四角形の座標は、合成画像の外側に配置できます。

四角形が遠近図形変換に適していない場合、動作は定義されません。 例えば、2つ以上の頂点が一致する場合、3つまたはすべての頂点が同じ線上にある場合、または四角形が自己交差または凹面である場合などです。

## 品質に関する考慮事項 {#section-7cc9056afa614300a9b8844d39739fc3}

デフォルトの実装では、品質とパフォーマンスの間に合理的な妥協点が生じますが、シャープを改善するためにソースイメージの解像度を上げたり、エイリアスアーティファクトを減らすためにソースイメージを減らしたりする必要がある場合があります。

ソースが画像の場合は、`scale=`を使用して別の解像度（画像の全解像度を基準とする）を選択します。 指定された`scale=`値は、次に高いPTIF解決レベルに丸められます。 ネストされたリクエストソースがある場合は、ネストされたリクエストによって生成される画像のサイズを調整して、目的のシャープさを実現できます。 テキストレイヤーの場合、入力画像（レンダリングされたテキスト）の解像度は、`textAttr=`で指定した解像度を上げて、大きなサイズ=値を選択することで調整されます。

修飾子&#x200B;*`resOptions`*&#x200B;を使用すると、代替の再サンプリングアルゴリズムを選択できます。 次の値がサポートされています（大文字と小文字を区別します）。

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>値</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> 最も近い隣人。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 双線形： </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 標準スーパーサンプリング（デフォルト）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 調整可能なジッター（<span class="varname"> n</span>のスーパーサンプリングは、0 ～ 200の整数値である必要があります）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-818e57df0a1b4449888543bc6af77751}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はレイヤー0に適用されます。 エフェクトレイヤーでは無視されます。

同じレイヤーに遠近法が存在する場合、修飾子`res=`は常に無視されます。 画像レイヤーに指定すると、修飾子`size=`は無視されます。 `perspective=`を持つレイヤーの修飾子`size=`と`res=`は、今後の使用のために予約されています。

## 初期設定 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`、遠近図形変換なし。

## 関連項目 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)、[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)、[pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)、[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
