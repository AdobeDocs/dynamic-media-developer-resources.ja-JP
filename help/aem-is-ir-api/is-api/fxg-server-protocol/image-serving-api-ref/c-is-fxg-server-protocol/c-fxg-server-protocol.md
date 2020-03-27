---
description: 基準点を使用してグラフィックを操作できます。基準点はコンパスの軸のように機能します。
seo-description: 基準点を使用してグラフィックを操作できます。基準点はコンパスの軸のように機能します。
seo-title: FXGサーバープロトコル
solution: Experience Manager
title: FXGサーバープロトコル
topic: Scene7 Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# FXGサーバープロトコル{#fxg-server-protocol}

基準点を使用してグラフィックを操作できます。基準点はコンパスの軸のように機能します。

基準点を使用すると、特定の基準点に基づいて、画像を回転、スケール、サイズ変更することができます。参照点は，,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,, `northWest``north``northEast``west``center``east``southWest``south``southeast`例えば、center 基準点を使用すると、基準点を中心にグラフィックを 45 度回転させることができます。以下の図は、基準点の位置、グラフィック、`northWest` 基準点から 20 度回転させた状態、`east` 基準点から 20 度回転させた状態を示しています。

![](assets/wp_ref_points.png)

* A.基準点の位置
* B.グラフィック
* C. The graphic rotated 20 degrees from its `northWest` reference point
* D. The graphic rotated 20 degrees from its `east` reference point

構文を次に示します。

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

初期設定値は none です。`inherit` 値は、`s7:referencePoint` でない場合に、ページまたはグループレベルの最上位からすべての子に `none` 値を渡します。`none` に設定した場合は、オブジェクトに基準点がなく、FXG 座標系が使用されていることを示します。

>[!NOTE]
>
>基準点を使用し、操作後にオブジェクトが移動しないようにするには、操作した後でオブジェクトの x と y の値を更新します。

`s7:referencePoint`   の値をグループ（またはパス、Line 要素または明確な幅と高さの定義がない任意の要素）とともに使用する場合は、値がグループの累積バウンディングボックスに適用されます。例えば、グループ内のすべてのオブジェクトのバウンディングボックスの左上の点はグループの `northWest` 基準点として機能し、右下の点は `southEast` 基準点として機能します。

