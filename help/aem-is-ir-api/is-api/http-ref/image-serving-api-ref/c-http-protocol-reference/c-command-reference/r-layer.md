---
description: '[画層]を選択します。 画層を選択し、コマンドシーケンスで新しい画層定義セグメントを開始します。'
solution: Experience Manager
title: 層
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---

# 層{#layer}

[画層]を選択します。 画層を選択し、コマンドシーケンスで新しい画層定義セグメントを開始します。

`layer= *``*|comp[, *`nname`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>選択するレイヤーの数（0以上）。 </p></td> 
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

画層セグメント内のすべてのコマンドが、指定した画層に適用されます。 レイヤーセグメントは、次の`layer=`コマンド、`effect=`コマンド、または要求の終了によって終了します。

`layer=comp`を指定して、合成画像（または一部のコマンドのビュー）を選択します。

レイヤ番号は、レイヤのz順序を効果的に指定します。 番号の大きいレイヤーは、番号の小さいレイヤーの上に配置されます。

画層番号は連続する必要はありません。 レイヤ0が必要です。

名前は、`layer= *`n`*, *`name`*`コマンドバリアントを使用してレイヤに割り当てることができます。 名前の付いたレイヤーを定義すると、レイヤー番号を知る必要なく、` layer= *`name`*`で参照できます。 複数の`layer= *`n`*, *`name`*`コマンドを使用して、同じレイヤに複数の名前を割り当てることができます。

>[!NOTE]
>
>レイヤ0は、合成キャンバスの全体的なサイズを決定します。 レイヤ0の境界の外にあるレイヤのすべての部分は、コンポジットを構築する際に切り抜かれます。

## プロパティ {#section-499963ee52c14f2898f0d0f90c1d01be}

レイヤコマンド `layer=`では代替変数の参照はサポートされていません。

`comp` は文字列として許可され *`name`* ません。同じ&#x200B;*`name`*&#x200B;が複数のレイヤーに割り当てられている場合、または以前に定義されていない&#x200B;*`name`*&#x200B;がレイヤーを参照している場合は、エラーが返されます。

## 初期設定 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. `layer=comp`の場合、多くのコマンドと属性がレイヤ0に適用されます。

## 特殊なケース {#section-e087cb2e3562473e8d391abfa3b9489f}

* 同じ名前が複数のレイヤにマッピングされる場合(例：`layer=1,image&layer=2,image`)の場合、エラーが発生します。
* 同じ名前が1つのレイヤに複数回マッピングされる場合(例：`layer=1,image&layer=1,image`)、範囲は通常どおりに設定され、エラーは発生しません。
* 同じ画層に対して複数の名前がサポートされます。

   レイヤーを参照する際に使用できる名前(例：`layer=1,image&layer=1,picture`)に置き換えます。
* 参照名がレイヤ番号にマッピングされない場合(例：`layer=1,image&layer=picture`)の場合、エラーが発生します。
* 代替変数は、レイヤー修飾子ではサポートされません(例：`layer=$image$`)に置き換えます。

   これは、画層名だけでなく、一般的な画層の修飾子にも適用されます。

* すべてのマージと上書きのルールは、同じレイヤーが複数のソースで参照されている場合と同じように機能する必要があります（リクエスト、プリまたはポストモディファイヤのカタログレコード、マクロなど）。

## 例 {#section-cc40de6a0a754178aa752601539c815b}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例を参照してください。
