---
description: テクスチャ繰り返しモード テクスチャイメージをタイル状にしてターゲットサーフェスを塗りつぶす方法を指定します。
seo-description: テクスチャ繰り返しモード テクスチャイメージをタイル状にしてターゲットサーフェスを塗りつぶす方法を指定します。
seo-title: Repeat
solution: Experience Manager
title: 繰り返し
topic: Scene7 Image Serving - Image Rendering API
uuid: bd15a573-9902-4672-992d-90d171160a46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 19%

---


# Repeat{#repeat}

テクスチャ繰り返しモード テクスチャイメージをタイル状にしてターゲットサーフェスを塗りつぶす方法を指定します。

## プロパティ {#section-cef4109cddf54ce095c3293d85bc412d}

列挙。 繰り返し可能なテクスチャにのみ使用します。 その他のマテリアルでは無視されます。

繰り返し可能なテクスチャマテリアルには、次の値を指定できます。

<table id="simpletable_C24FDA80A8AC431DA3FC86188E3774E1" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>0 </p></td> 
  <td class="- topic/stentry stentry"> <p>ストレートリピート。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>1 </p></td> 
  <td class="- topic/stentry stentry"> <p>4方向のランダムタイリング。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>2 </p></td> 
  <td class="- topic/stentry stentry"> <p>8方向のランダムタイリング。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>3 </p></td> 
  <td class="- topic/stentry stentry"> <p>ひし形のタイリング。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>4 </p></td> 
  <td class="- topic/stentry stentry"> <p>壁紙が四分の一滴下になる。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>5 </p></td> 
  <td class="- topic/stentry stentry"> <p>3滴目の壁紙が掛かる。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>6 </p></td> 
  <td class="- topic/stentry stentry"> <p>壁紙を半ドロップで掛ける。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>7 </p></td> 
  <td class="- topic/stentry stentry"> <p>5滴目の壁紙が掛かる。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>8 </p></td> 
  <td class="- topic/stentry stentry"> <p>壁紙のハングを元に戻します。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>9 </p></td> 
  <td class="- topic/stentry stentry"> <p>ランダムな壁紙がハングします。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>10 </p></td> 
  <td class="- topic/stentry stentry"> <p>ランダムドロップ。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>11 </p></td> 
  <td class="- topic/stentry stentry"> <p>ランダムに横切る。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>12 </p></td> 
  <td class="- topic/stentry stentry"> <p>半分横。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>13 </p></td> 
  <td class="- topic/stentry stentry"> <p>鏡像（ブックマッチ） </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>14 </p></td> 
  <td class="- topic/stentry stentry"> <p>標準のランダム化機能 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>15 </p></td> 
  <td class="- topic/stentry stentry"> <p>高周波ランダム化器 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>16 </p></td> 
  <td class="- topic/stentry stentry"> <p>低周波のランダム化器 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>17 </p></td> 
  <td class="- topic/stentry stentry"> <p>水平方向のランダム化 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>18 </p></td> 
  <td class="- topic/stentry stentry"> <p>垂直方向のランダム化 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>19 </p></td> 
  <td class="- topic/stentry stentry"> <p>エッジのランダム化 </p></td> 
 </tr> 
</table>

## 初期設定 {#section-23fba3bd1f3544c7913d12f2ca148517}

0（ストレートリピート）

## 関連項目 {#section-a08887a91db34ed3b183899c69c9f74f}

[リピート=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8)
