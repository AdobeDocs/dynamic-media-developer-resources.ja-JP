---
title: リピート
description: テクスチャの繰り返しモード 繰り返し可能なテクスチャ マテリアルの繰り返しモードを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6cc82742-4ba0-4524-a87b-586539d7fe38
TQID: 'https://experienceleague.adobe.com/7UAuemyiN3GQKpDUkkRsHiRaLh1w7Lx8s5dkUw25-eM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 15%

---

# リピート{#repeat}

テクスチャの繰り返しモード 繰り返し可能なテクスチャ マテリアルの繰り返しモードを指定します。

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>ストレートの繰り返し。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>4方向ランダムタイリング。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>8方向ランダムタイリング。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>ダイヤモンドタイリング。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>クォータードロップ壁紙ぶら下がり。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>3番目のドロップ壁紙ぶら下がっています。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>ハーフドロップ壁紙ぶら下がり。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>5番目のドロップの壁紙ぶら下がっています。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>壁紙ぶら下がりを逆にする。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>ランダムな壁紙ぶら下がり。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>ランダムドロップ： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>ランダムに移動します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>半分を横切る。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>ミラー（ブックマッチ）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>標準ランダマイザー： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>高周波ランダマイザー。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>低周波ランダマイザー。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>水平ランダマイザー： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>垂直ランダマイザー： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Edge randomizer. </p> </td> 
 </tr> 
</table>

ランダムキルティングモード（14....18）は、容易に繰り返すことができない画像からテクスチャを合成するために使用することができ、アルゴリズムは、元の画像に基づいて完全にランダムまたは部分的にランダムなテクスチャを生成する。

## プロパティ {#section-262bf540930d4890b678ea00cefe1909}

マテリアル属性： 単色、デカール、キャビネットのマテリアルでは無視されます。

## 初期設定 {#section-e5bbd7d9fbb74852849e605d20f550bb}

資料がカタログ エントリに基づいている場合は`catalog::Repeat`、それ以外の場合は`0` （ストレート）。

## 関連項目 {#section-ac99113b64654d75a3a86e41db546269}

[catalog::Repeat](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)

