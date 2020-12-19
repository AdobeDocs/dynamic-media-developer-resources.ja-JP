---
description: '[画層]を選択します。 画層を選択し、コマンドシーケンス内の新しい画層定義セグメントを開始します。'
seo-description: '[画層]を選択します。 画層を選択し、コマンドシーケンス内の新しい画層定義セグメントを開始します。'
seo-title: layer
solution: Experience Manager
title: layer
topic: Scene7 Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# layer{#layer}

[画層]を選択します。 画層を選択し、コマンドシーケンス内の新しい画層定義セグメントを開始します。

`layer= *``*|comp[, *`名前`*]`

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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>レイヤー名. </p></td> 
 </tr> 
</table>

レイヤーセグメント内のすべてのコマンドが、指定したレイヤーに適用されます。 レイヤーセグメントは、次の`layer=`または`effect=`コマンド、または要求の終わりによって終了します。

`layer=comp`を指定して、合成画像(または一部のコマンドの表示)を選択します。

レイヤー番号は、レイヤーのz順序を効果的に指定します。 番号の大きいレイヤーは、番号の小さいレイヤーの上に配置されます。

レイヤー番号を連続させる必要はありません。 レイヤー0が必要です。

`layer= *`n`*, *`name`*`コマンドバリアントを使用して、レイヤーに名前を割り当てることができます。 名前の付いた画層を定義すると、` layer= *`name`*`で参照できます。画層番号を知る必要はありません。 複数の`layer= *`n`*, *`name`*`コマンドを使用して、同じレイヤに複数の名前を割り当てることができます。

>[!NOTE]
>
>レイヤ0は、合成キャンバスの全体的なサイズを決定します。 レイヤー0の境界の外にあるレイヤーのすべての部分は、合成を構築する際に切り抜かれます。

## プロパティ {#section-499963ee52c14f2898f0d0f90c1d01be}

レイヤーコマンド `layer=`では、代替変数の参照はサポートされていません。

`comp` は、 *`name`* 文字列として使用できません。同じ&#x200B;*`name`*&#x200B;が複数のレイヤーに割り当てられている場合、またはレイヤーが以前に定義されていない&#x200B;*`name`*&#x200B;によって参照されている場合は、エラーが返されます。

## 初期設定 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. `layer=comp`の場合、多くのコマンドと属性がレイヤ0に適用されます。

## 特殊ケース{#section-e087cb2e3562473e8d391abfa3b9489f}

* 同じ名前が複数のレイヤーにマップされる場合(例：`layer=1,image&layer=2,image`)が含まれている場合、エラーが発生します。
* 同じ名前が1つのレイヤに複数回マップされる場合(例：`layer=1,image&layer=1,image`)の場合、範囲は通常どおりに設定され、エラーは発生しません。
* 同じレイヤーに対して複数の名前がサポートされます。

   レイヤーの参照には、次の名前を使用できます。`layer=1,image&layer=1,picture`)。
* 参照名がレイヤー番号にマップされない場合(例：`layer=1,image&layer=picture`)が含まれている場合、エラーが発生します。
* 代替変数は、レイヤー修飾子ではサポートされません(例：`layer=$image$`)。

   これは、レイヤ名だけでなく、一般的なレイヤモディファイヤに適用されるすべての順列に適用されます。

* すべての結合および上書きルールは、同じレイヤーが複数のソース（リクエスト、モディファイヤのカタログレコードまたはPOST、マクロなど）で参照されている場合とまったく同じように機能します。

## 例 {#section-cc40de6a0a754178aa752601539c815b}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例を参照してください。
