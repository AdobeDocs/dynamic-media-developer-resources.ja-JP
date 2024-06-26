---
description: textPs=は、この節で説明する様々な使用モデルの数をサポートしています。
solution: Experience Manager
title: テキストレイヤー
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# テキストレイヤー{#text-layers}

textPs=は、この節で説明する様々な使用モデルの数をサポートしています。

>[!NOTE]
>
>この節の内容は次の場合には適用されません。 `text=`.

一般的なルールと定義は次のとおりです。

* セルフサイズのテキストレイヤーとは、 `size=` コマンドまたはの `size=0,0` が指定されている。

* セルフサイズのテキストレイヤーのレイヤーサイズは、レンダリングされる実際のテキストによって決まります。
* 通常、自己サイズのテキストレイヤーのデフォルトのレイヤーアンカーは *ではない* レイヤーの中央（以下を参照）。
* 次の場合 `anchor=` または `origin=` がセルフサイズのテキストレイヤーに指定されている場合、テキストレイヤーの位置はテキストコンテンツの影響を受けます。

* 条件 `size=` を指定すると、文字記号の一部がレイヤーの長方形の外側にレンダリングされる場合があります。
* `pos=` は、どのような場合でもテキストレイヤーの位置を変更するために使用できます。

## ポイントテキスト（セルフサイズ設定） {#section-db99ec98eb114458b2dbc9911a58f74a}

Photoshop スタイルのポイントテキストは、次の場合にシミュレートされます `textPs=` 指定しない `size=`, `textPath=`、または `textFlowPath=`. レイヤーのサイズは、レンダリングされるテキストの幅によって水平方向に、行間隔によって垂直方向に決まります。 テキストは自動的に折り返されません。

どちらでもない場合 `anchor=` nor `origin=` を指定すると、テキストの最初の行がレイヤーの基準点のすぐ上に配置されます。でマークされた段落です。 `\ql` 次の段落を含むレイヤーの基準点の右側に配置されます `\qr` 元の段落の左側にレンダリングされ、次の段落が含まれます `\qc` 原点を中心に水平方向に配置します。 次の場合は、標準のレイヤーの配置規則が適用されます `anchor=` または `origin=` が指定されている。

次の場合 `color=` を指定すると、レンダリングされる実際のテキストのバウンディングボックス全体が表示されます。

次の RTF コマンドは無視されます。 `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## 矩形テキストボックス {#section-1d3ab11df26d4004a1a801546756475d}

次の場合 `size=` に加えてが指定されています。 `textPs=` （なし `textPath=` および `textFlowPath=`）、テキストは指定した長方形に制限されます。 レイヤーの位置は通常どおり設定されます。 テキストボックスのエッジ付近にある文字記号は、テキストボックスの外側に部分的にレンダリングされる場合があります。

`color=` によって定義された領域を埋める `size=`.

すべての RTF コマンドが期待どおりに適用されます。

## 「可変高」テキスト・ボックス {#section-e1233d1c9f8e43218667361dc0c4fd06}

指定 `size=` 高さが 0 の場合、テキスト ボックスのサイズを垂直方向に変更して、すべての内容に合わせることができます。 レイヤーの幅は、次の幅で定義されます `size=`と、実際にレンダリングされたテキストの高さによるレイヤーの高さ。 レイヤーの位置は通常どおり設定されます。 テキストボックスの左右の端に近い文字記号は、テキストボックスの外側に部分的にレンダリングされる場合があります。

`color=` で指定された幅で定義された長方形を塗りつぶします `size=` レンダリングされる実際のテキストの高さです。

次の RTF コマンドは無視されます。

`\vertal*`

## パス内の自己サイズ設定テキスト {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` ～と関連して `textPs=` テキストを流し込む 1 つ以上の領域を定義するために使用できます。 `textFlowXPath=` 1 つ以上の領域へのテキストの流れ込みを除外するために、オプションで指定できます。 次の場合 `size=` が指定されていない場合、生成されるテキストレイヤーはセルフサイズになり、レイヤーサイズは実際にレンダリングされるテキストのバウンディングボックスによって決定されます。

どちらでもない場合 `origin=` nor `anchor=` を指定すると、レイヤーアンカーはデフォルトでパスの定義に使用されるピクセル座標空間（0,0）になり、レンダリングされたテキストに関係なく絶対的な位置を確保します。 次の場合 `anchor=` または `origin=` を指定すると、レイヤーは、レンダリングされる実際のコンテンツのバウンディングボックスを基準にして（そしてバウンディングボックスに適応して）配置されます。

`color=` レンダリングされた実際のテキストのバウンディングボックスを塗りつぶします。

次の RTF コマンドは無視されます。

`\marg*`

## パス内の事前サイズ設定されたテキスト {#section-ed492a8a54414cd4bde360500cec6968}

次の場合 `size=` と共に指定されます。 `textFlowPath=`の場合、レイヤーサイズは事前に決定されています。 パスの定義に使用するピクセル座標空間の（0,0）は、レイヤーの長方形の左上隅に配置されます。

この `textFlowPath=` 領域は、画層の長方形の外側に配置できます。 テキストは、レイヤーの長方形の外側にレンダリングされる結果となる場合でも、常にすべてのパス領域にフローおよびレンダリングされます。 `extend=0,0,0,0`を使用して、レンダリングしたテキストをレイヤーの長方形に切り抜くことができます。

レイヤーの配置目的で、レイヤーの長方形は指定されたに基づきます `size=`実際にレンダリングされるテキストの量に関係なく、一部がレイヤーの長方形の外側にある場合でも同様です。 標準のレイヤー配置が適用されます。

`color=` で定義された矩形領域を塗り潰します。 `size=`.

次の RTF コマンドは、 `textFlowPath=`:

`\marg*`

## パス上の自己サイズ設定テキスト {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` で指定されたテキストの参照先となる 1 つ以上のパスを定義します。 `textPs=` をレンダリングする必要があります。 条件 `size=` が指定されていない場合、生成されるテキストレイヤーはセルフサイズ設定になります。 レイヤーサイズは、レンダリングされる実際のテキストのバウンディングボックスによって決まります。

どちらでもない場合 `origin=` nor `anchor=` を指定すると、レイヤーアンカーはデフォルトで、パスを定義するために使用されるピクセル座標空間（0,0）になります。レンダリングされるテキストの位置は、レンダリングされるテキストの量に関係なく固定されます。 次の場合 `anchor=` または `origin=` を指定すると、レイヤーは、レンダリングされる実際のコンテンツのバウンディングボックスを基準にして（そしてバウンディングボックスに適応して）配置されます。

`color=` レンダリングされた実際のテキストのバウンディングボックスを塗りつぶします。

次の RTF コマンドは無視されます。

* `\marg*`
* `\hyph*`
* `\vertal*`

最初のの後のテキスト `\par` または `\line` は無視されます。

## パス上の事前サイズ設定されたテキスト {#section-a3bbbc5187f448b192e53d27e2c53f2f}

次の場合 `size=` と共に指定されます。 `textPath=`の場合、レイヤーサイズは事前に決定されています。 パスの定義に使用するピクセル座標空間の（0,0）は、レイヤーの長方形の左上隅に配置されます。

パスは、レイヤーの長方形の一部または全体の外側に配置できます。 テキストは、レイヤーの長方形の外側にあっても、常にパス全体に沿って適用およびレンダリングされます。 `extend=0,0,0,0` を使用して、レンダリングしたテキストをレイヤーの長方形に切り抜くことができます。

レイヤーの配置目的で、レイヤーの長方形は指定されたに基づきます `size=`テキストの一部がレイヤーの長方形の外側にレンダリングされている場合でも同様です。 標準のレイヤー配置が適用されます。

`color=` で定義された領域を塗りつぶします。 `size=`.

次の RTF コマンドは無視されます。

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

最初のの後のテキスト `\par` または `\line` は無視されます。
