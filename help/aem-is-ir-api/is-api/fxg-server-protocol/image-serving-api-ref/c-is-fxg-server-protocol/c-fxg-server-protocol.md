---
title: FXG サーバープロトコル
description: 基準点を使用してグラフィックを操作できます。基準点はコンパスの軸のように機能します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 69%

---

# FXG サーバープロトコル{#fxg-server-protocol}

基準点を使用してグラフィックを操作できます。基準点はコンパスの軸のように機能します。

基準点を使用すると、特定の基準点に基づいて、画像を回転、スケール、サイズ変更することができます。基準点は `northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`、`southeast` です。 たとえば、中心の基準点を使用すると、グラフィックを中心に 45 °回転できます。 次の図は、基準点の位置、図、`northWest` 基準点から 20°回転した図、`east` 基準点から 20°回転した図を示しています。

![基準点のイメージ](assets/wp_ref_points.png)

* A.基準点の位置
* ロ。図
* C.図形が `northWest` 基準点から 20°回転した状態
* D.図形が `east` 基準点から 20°回転した状態

構文を次に示します。

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

初期設定値は none です。`inherit` 値は、`s7:referencePoint` でない場合に、ページまたはグループレベルの最上位からすべての子に `none` 値を渡します。`none` に設定した場合は、オブジェクトに基準点がなく、FXG 座標系が使用されていることを示します。

>[!NOTE]
>
>基準点を使用し、操作後にオブジェクトが移動しないようにするには、操作した後でオブジェクトの x と y の値を更新します。

`s7:referencePoint`   の値をグループ（またはパス、Line 要素または明確な幅と高さの定義がない任意の要素）とともに使用する場合は、値がグループの累積バウンディングボックスに適用されます。例えば、グループ内のすべてのオブジェクトのバウンディングボックスの左上の点はグループの `northWest` 基準点として機能し、右下の点は `southEast` 基準点として機能します。
