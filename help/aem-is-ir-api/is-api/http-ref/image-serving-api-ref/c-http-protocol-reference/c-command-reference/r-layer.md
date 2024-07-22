---
title: レイヤー
description: 「レイヤー」を選択します。 画層を選択し、コマンド シーケンスで新しい画層定義セグメントを開始します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# レイヤー{#layer}

「レイヤー」を選択します。 画層を選択し、コマンド シーケンスで新しい画層定義セグメントを開始します。

`layer= *`n`*|comp[, *`name`*]`

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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> の名前 </span></span> </p></td> 
  <td class="stentry"> <p>レイヤー名。 </p></td> 
 </tr> 
</table>

画層セグメント内のすべてのコマンドは、指定した画層に適用されます。 画層セグメントは、次の `layer=` または `effect=` コマンド、または要求の終了によって終了します。

合成イメージ（または一部のコマンドではビュー）を選択する `layer=comp` を指定します。

レイヤ番号は、レイヤの Z オーダーを効果的に指定します。 番号の大きいレイヤーは、番号の小さいレイヤーの上に配置されます。

レイヤ番号は連続している必要はありません。 レイヤ 0 が必要です。

`layer= *`n`*, *`name`*` コマンド バリアントを使用して、画層に名前を割り当てることができます。 名前の付いたレイヤを定義すると、レイヤ番号を知らなくても、そのレイヤを ` layer= *`name`*` で参照できます。 複数の `layer= *`n`*, *`name`*` コマンドを使用して、同じレイヤーに複数の名前を割り当てることができます。

>[!NOTE]
>
>レイヤ 0 は、合成キャンバスの全体のサイズを決定します。 合成が作成されると、レイヤ 0 の境界の外側にあるレイヤのすべての部分が切り抜かれます。

## プロパティ {#section-499963ee52c14f2898f0d0f90c1d01be}

[ 画層 ] コマンド： 代替変数参照は `layer=` ではサポートされていません。

`comp` は *`name`* 文字列として許可されていません。 同じ *`name`* が複数の画層に割り当てられている場合、または以前に定義されていない *`name`* によって画層が参照されている場合は、エラーが返されます。

## 初期設定 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`。 多くのコマンドと属性は、レイヤ 0 に適用されます（`layer=comp` の場合）。

## 特殊ケース {#section-e087cb2e3562473e8d391abfa3b9489f}

* 同じ名前が複数のレイヤーにマッピングされている場合（例：`layer=1,image&layer=2,image`）、エラーが発生します。
* 同じ名前が 1 つのレイヤーに複数回マッピングされる場合（例：`layer=1,image&layer=1,image`）、範囲はエラーなしで通常どおりに設定されます。
* 同じレイヤーに複数の名前を付けることができます。

  どちらの名前を使用しても、レイヤーを参照できます（例：`layer=1,image&layer=1,picture`）。
* 参照名がレイヤ番号にマッピングされていない場合（例：`layer=1,image&layer=picture`）、エラーが発生します。
* レイヤー修飾子では、代替変数はサポートされていません（例：`layer=$image$`）。

  これは、レイヤ名だけでなく、一般的なレイヤ モディファイヤにも適用されます。

* すべての結合ルールと上書きルールは、同じレイヤーが複数のソース（リクエスト、修飾子カタログレコードの前または後、マクロなど）で参照される場合と同じように機能します。

## 例 {#section-cc40de6a0a754178aa752601539c815b}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の例を参照してください。
