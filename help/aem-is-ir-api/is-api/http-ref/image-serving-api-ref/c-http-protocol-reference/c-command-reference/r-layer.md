---
title: レイヤー
description: '[ 画層 ] を選択します。 画層を選択し、コマンドシーケンスで新しい画層定義セグメントを開始します。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---

# レイヤー{#layer}

[ 画層 ] を選択します。 画層を選択し、コマンドシーケンスで新しい画層定義セグメントを開始します。

`layer= *`n`*|comp[, *`名前`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>選択するレイヤーの数（0 以上）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>合成画像を選択します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名前</span></span> </p></td> 
  <td class="stentry"> <p>レイヤー名. </p></td> 
 </tr> 
</table>

画層セグメント内のすべてのコマンドが、指定した画層に適用されます。 画層セグメントは次の `layer=` または `effect=` コマンドを使用するか、リクエストの最後に配置します。

指定 `layer=comp` をクリックして、合成イメージ（または一部のコマンドのビュー）を選択します。

レイヤ番号は、レイヤの z 順序を効果的に指定します。 高い番号のレイヤーは、下の番号のレイヤーの上に配置されます。

画層番号は連続する必要はありません。 レイヤ 0 が必要です。

名前は、 `layer= *`n`*, *`名前`*` コマンドのバリアント。 名前の付いた画層を定義すると、その画層はで参照できます。 ` layer= *`名前`*`（レイヤー番号を知る必要はありません）。 複数の名前を同じ画層に割り当てることができます。複数の名前を使用します `layer= *`n`*, *`名前`*` コマンド

>[!NOTE]
>
>レイヤ 0 は、合成キャンバスの全体的なサイズを決定します。 レイヤ 0 の境界の外にあるレイヤのすべての部分は、コンポジットを構築する際に切り抜かれます。

## プロパティ {#section-499963ee52c14f2898f0d0f90c1d01be}

[ 画層 ] コマンド 代替変数の参照は、 `layer=`.

`comp` は、 *`name`* 文字列。 同じ *`name`* が複数の画層に割り当てられているか、画層が次の基準で参照されている場合 *`name`* は以前に定義されていません。

## 初期設定 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 次の場合、多くのコマンドと属性がレイヤ 0 に適用されます。 `layer=comp`.

## 特例 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 同じ名前が複数の画層にマッピングされる場合 ( 例： `layer=1,image&layer=2,image`) の場合、エラーが発生します。
* 同じ名前が 1 つの画層に複数回マッピングされる場合 ( 例： `layer=1,image&layer=1,image`) の場合、範囲は通常どおりに設定され、エラーは発生しません。
* 同じ画層に対して複数の名前がサポートされます。

   レイヤーを参照するために使用できる名前 ( 例： `layer=1,image&layer=1,picture`) をクリックします。
* 参照名がレイヤ番号にマッピングされない場合 ( 例： `layer=1,image&layer=picture`) の場合、エラーが発生します。
* 代替変数は、レイヤー修飾子ではサポートされません ( 例： `layer=$image$`) をクリックします。

   これは、画層名だけでなく、一般に画層の修飾子にも当てはまります。

* すべてのマージルールと上書きルールは、同じレイヤーが複数のソースで参照されている場合（リクエスト、モディファイヤーのカタログレコード、マクロなど）と同じように機能する必要があります。

## 例 {#section-cc40de6a0a754178aa752601539c815b}

詳しくは、 [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
