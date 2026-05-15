---
title: レイヤー
description: レイヤーを選択します。 レイヤーを選択し、コマンドシーケンスで新しいレイヤー定義セグメントを開始します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
TQID: 'https://experienceleague.adobe.com/7RMSQNrhGOufvbqHQFB6ow-PA1z-RoLtuolmUoAlGoA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 387
ht-degree: 0%

---

# レイヤー{#layer}

レイヤーを選択します。 レイヤーを選択し、コマンドシーケンスで新しいレイヤー定義セグメントを開始します。

`layer= *`n`*|comp[, *`の名前`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>選択するレイヤーの数（0以上）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> コンポジション </span> </p></td> 
  <td class="stentry"> <p>合成画像を選択します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">名</span></span> </p></td> 
  <td class="stentry"> <p>レイヤー名。 </p></td> 
 </tr> 
</table>

レイヤーセグメント内のすべてのコマンドは、指定したレイヤーに適用されます。 レイヤーセグメントは、次の`layer=`または`effect=` コマンドまたはリクエストの最後で終了します。

`layer=comp`を指定して、コンポジット画像（または一部のコマンドのビュー）を選択します。

レイヤー番号は、レイヤーのZ次を効果的に指定します。 番号の高いレイヤーは、番号の低いレイヤーの上に配置されます。

レイヤー番号は連続する必要はありません。 レイヤー0が必要です。

名前は、`layer= *`n`*, *`name`*` コマンド バリアントを持つレイヤーに割り当てることができます。 名前付きレイヤーを定義すると、レイヤー番号を知らなくても` layer= *`name`*`で参照できます。 複数の`layer= *`n`*, *`name`*` コマンドを使用して、同じレイヤーに複数の名前を割り当てることができます。

>[!NOTE]
>
>レイヤー0は、合成キャンバスの全体的なサイズを決定します。 コンポジットを構築すると、レイヤー0の境界の外側にあるレイヤーのすべての部分が切り抜かれます。

## プロパティ {#section-499963ee52c14f2898f0d0f90c1d01be}

Layer コマンド。 `layer=`では、置換変数の参照はサポートされていません。

`comp`は&#x200B;*`name`*&#x200B;文字列として許可されていません。 同じ&#x200B;*`name`*&#x200B;が複数のレイヤーに割り当てられている場合、またはレイヤーが以前に定義されていない&#x200B;*`name`*&#x200B;によって参照されている場合は、エラーが返されます。

## 初期設定 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. `layer=comp`の場合、レイヤー0には多くのコマンドと属性が適用されます。

## 特殊ケース {#section-e087cb2e3562473e8d391abfa3b9489f}

* 同じ名前が複数のレイヤーにマッピングされている場合（例：`layer=1,image&layer=2,image`）、エラーが発生します。
* 同じ名前が単一のレイヤーに複数回マッピングされている場合（例：`layer=1,image&layer=1,image`）、スコープはエラーなしで通常どおりに設定されます。
* 同じレイヤーの複数の名前がサポートされています。

  どちらの名前でもレイヤーを参照できます（例：`layer=1,image&layer=1,picture`）。
* 参照名がレイヤー番号にマッピングされない場合（例：`layer=1,image&layer=picture`）、エラーが発生します。
* 置換変数は、レイヤー修飾子ではサポートされていません（例：`layer=$image$`）。

  これは、レイヤー名だけでなく、一般的にレイヤー修飾子に対するすべての置換に適用されます。

* すべての結合ルールとオーバーライドルールは、同じレイヤーが複数のソース（リクエスト、修飾子の前後のカタログレコード、マクロなど）で参照されている場合と同じように機能する必要があります。

## 例 {#section-cc40de6a0a754178aa752601539c815b}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例を参照してください。
