---
title: FXG サーバープロトコル
description: グラフィックを操作するには、コンパス点と同様の参照点を使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 18%

---

# FXG サーバープロトコル{#fxg-server-protocol}

グラフィックを操作するには、コンパス点と同様の参照点を使用できます。

基準点を使用すると、特定の基準点に基づいて、画像を回転、スケール、サイズ変更することができます。基準点は、`northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`、`southeast` です。 例えば、中心基準点を使用すると、グラフィックをその中心で 45 度回転できます。 次の図に、基準点の位置、グラフィック、`northWest` の基準点から 20°回転したグラフィック、および `east` の基準点から 20°回転したグラフィックを示します。

![ 基準点の画像 ](assets/wp_ref_points.png)

* A.参照点の位置
* ロ。グラフィック
* C. グラフィックが `northWest` の基準点から 20°回転します
* D. グラフィックが `east` の基準点から 20 度回転します

構文を次に示します。

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

デフォルト値は「なし」です。 `inherit` の値は、`s7:referencePoint` でない限り、ページまたはグループレベルの最上位からすべての子に `none` の値を渡します。 `none` の設定は、オブジェクトの基準点がなく、FXG 座標系が使用されることを意味します。

>[!NOTE]
>
>基準点を使用し、操作後にオブジェクトが移動しないようにするには、操作した後でオブジェクトの x と y の値を更新します。

`s7:referencePoint` の値がグループ（または、パス、線要素、または明示的な幅と高さの定義を持たない要素）で使用されている場合、その値はグループの累積境界ボックスに適用されます。 たとえば、グループ内のすべてのオブジェクトの境界ボックスの左上の点は、グループの `northWest` の基準点として機能します。右下の点は、`southEast` の基準点として機能します。
