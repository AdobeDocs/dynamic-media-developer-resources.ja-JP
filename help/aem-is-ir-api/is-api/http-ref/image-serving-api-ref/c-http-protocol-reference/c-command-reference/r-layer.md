---
description: 「レイヤー」を選択します。 画層を選択し、コマンドシーケンスで新しい画層定義セグメントを開始します。
seo-description: 「レイヤー」を選択します。 画層を選択し、コマンドシーケンスで新しい画層定義セグメントを開始します。
seo-title: 層
solution: Experience Manager
title: 層
topic: Scene7 Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# layer{#layer}

「レイヤー」を選択します。 画層を選択し、コマンドシーケンスで新しい画層定義セグメントを開始します。

`layer= *`名`*|comp[, *`前`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>選択するレイヤーの数（0以上の整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>合成画像を選択します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名</span></span> </p></td> 
  <td class="stentry"> <p>レイヤー名. </p></td> 
 </tr> 
</table>

レイヤーセグメント内のすべてのコマンドが、指定したレイヤーに適用されます。 レイヤーセグメントは、次のコマンドまたはコ `layer=` マンド、 `effect=` または要求の最後で終了します。

一部のコ `layer=comp` マンドの合成画像（またはビュー）を選択する場合に指定します。

レイヤー番号は、レイヤーのz順序を効果的に指定します。 大きい番号のレイヤーは、小さい番号のレイヤーの上に配置されます。

レイヤー番号は連続している必要はありません。 レイヤー0が必要です。

名前は、nameコマンドバリアントを使用して画層に割り当て `layer= *``*, *`るこ`*` とができます。 名前の付いた画層を定義すると、その画層を ` layer= *`名前で参照でき`*`、画層番号を知る必要はありません。 複数の名前コマンドを使用して、同じ画層に複数の名前を割り当てるこ `layer= *``*, *`とができ`*` ます。

>[!NOTE]
>
>レイヤ0は、合成キャンバスの全体的なサイズを決定します。 レイヤー0の境界の外にあるレイヤーのすべての部分は、合成を構築する際に切り抜かれます。

## プロパティ {#section-499963ee52c14f2898f0d0f90c1d01be}

レイヤーコマンド では、代替変数の参照はサポートされていませ `layer=`ん。

`comp` は文字列として許可されてい *`name`* ません。 同じ画層が複数の画層に割り当てら *`name`* れている場合、または画層が参照されていて、以前に定義されていな *`name`* い場合は、エラーが返されます。

## 初期設定 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 多くのコマンドと属性は、レイヤー0に適用されま `layer=comp`す。

## 特例 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 同じ名前が複数のレイヤーにマップされる場合(例： `layer=1,image&layer=2,image`)の場合、エラーが発生します。
* 同じ名前が1つのレイヤーに複数回マップされる場合(例： `layer=1,image&layer=1,image`)の場合、範囲は通常どおりに設定され、エラーは発生しません。
* 同じレイヤーに対する複数の名前がサポートされます。

   レイヤーを参照する際に使用できる名前(例： `layer=1,image&layer=1,picture`)。
* 参照名がレイヤー番号にマップされない場合(例： `layer=1,image&layer=picture`)の場合、エラーが発生します。
* 置換変数は、レイヤー修飾子ではサポートされません(例： `layer=$image$`)。

   これは、画層名だけでなく、一般的な画層修飾子にも、すべての順列に適用されます。

* すべての結合および上書きルールは、同じレイヤーが複数のソース（リクエスト、モディファイヤカタログレコード前または後のレコード、マクロなど）で参照されている場合とまったく同じように機能します。

## 例 {#section-cc40de6a0a754178aa752601539c815b}

テンプレートの例を参照して [ください](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。
