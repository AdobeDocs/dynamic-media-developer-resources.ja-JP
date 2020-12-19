---
description: マテリアルサーフェスタイプ マテリアルのサーフェスタイプを指定します。
seo-description: マテリアルサーフェスタイプ マテリアルのサーフェスタイプを指定します。
seo-title: タイプ
solution: Experience Manager
title: タイプ
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f107d50-b363-4670-bb02-873677e7bbea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 22%

---


# タイプ{#type}

マテリアルサーフェスタイプ マテリアルのサーフェスタイプを指定します。

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>不明、サーバーはデフォルトを使用 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>その他 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>天然木材 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>研磨金属 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>ブラシ付き金属 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>古い金属 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>ペイント </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>エナメル/ラッカー </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>壁紙 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p></td> 
  <td class="stentry"> <p>プラスチック </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p></td> 
  <td class="stentry"> <p>ソリッドサーフェス </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p></td> 
  <td class="stentry"> <p>ラミネート </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p></td> 
  <td class="stentry"> <p>ビニール </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p></td> 
  <td class="stentry"> <p>セラミック </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p></td> 
  <td class="stentry"> <p>天然石 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p></td> 
  <td class="stentry"> <p>ガラス </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p></td> 
  <td class="stentry"> <p>ミラー </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p></td> 
  <td class="stentry"> <p>織物 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p></td> 
  <td class="stentry"> <p>薄い生地 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p></td> 
  <td class="stentry"> <p>カーペット </p></td> 
 </tr> 
</table>

`gloss=`と`rough=`を組み合わせて使用し、反射と光沢効果の動作を制御します。 `gloss=`と`rough=`が同じであっても、異なるマテリアルは異なる効果を生み出します。

## プロパティ {#section-2345b2508273426295ce8ac46182ea64}

マテリアル属性 ビネットに3-D反射データが含まれていない場合、またはビネットで光沢効果が無効な場合は無視されます。

## 初期設定 {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` 材料がカタログエントリに基づいている場合。それ以外の場合は`type=0`。 指定しなかった場合、または`type=0`の場合、サーバはターゲットオブジェクトと他のマテリアル属性に応じて適切なデフォルトを選択します。

## 関連項目 {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 、 [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
