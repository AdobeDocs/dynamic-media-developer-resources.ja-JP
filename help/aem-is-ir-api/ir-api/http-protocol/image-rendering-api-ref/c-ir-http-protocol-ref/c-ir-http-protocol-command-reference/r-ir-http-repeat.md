---
description: テクスチャ繰り返しモード 繰り返し可能なテクスチャマテリアルの繰り返しモードを指定します。
seo-description: テクスチャ繰り返しモード 繰り返し可能なテクスチャマテリアルの繰り返しモードを指定します。
seo-title: リピート
solution: Experience Manager
title: リピート
topic: Scene7 Image Serving - Image Rendering API
uuid: 6508fdff-27cd-4038-b506-39b927f3526a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# リピート{#repeat}

テクスチャ繰り返しモード 繰り返し可能なテクスチャマテリアルの繰り返しモードを指定します。

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>ストレートリピート。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>4方向のランダムタイリング。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>8方向のランダムタイリング。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>ひし形タイリング。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>壁紙が垂れ下がる </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>3滴目の壁紙がぶら下がる。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>壁紙を半滴で張る。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>5滴目の壁紙がぶら下がる。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>壁紙を裏返しにします。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>ランダムな壁紙がハングする。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>ランダムドロップ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>ランダム。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>半分横。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>鏡像化(bookmatch) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>標準のランダム化 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>高周波のランダム化 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>低周波のランダム化 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>水平方向のランダム化 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>垂直方向のランダム化 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>エッジのランダム化 </p> </td> 
 </tr> 
</table>

ランダムキルティングモード(14...18)は、容易に繰り返しが可能でない画像からテクスチャを合成するために使用できる。アルゴリズムは、元のイメージに基づいて、完全にランダムまたは部分的にランダムなテクスチャを作成します。

## プロパティ {#section-262bf540930d4890b678ea00cefe1909}

マテリアル属性。 ソリッドカラー、デカル、キャビネットのマテリアルでは無視されます。

## 初期設定 {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`に基づくマテリアルの場合は、カタログエントリに基づくマテリアルの場合は、それ以外の場合は `0` （まっすぐな繰り返し）。

## 関連項目 {#section-ac99113b64654d75a3a86e41db546269}

[catalog::Repeat](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
