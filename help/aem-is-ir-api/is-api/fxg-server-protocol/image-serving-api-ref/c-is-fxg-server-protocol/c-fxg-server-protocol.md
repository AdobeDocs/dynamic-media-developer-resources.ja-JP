---
title: FXG サーバープロトコル
description: 基準点を使用してグラフィックを操作できます。基準点はコンパスの軸のように機能します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# FXG サーバープロトコル{#fxg-server-protocol}

基準点を使用してグラフィックを操作できます。基準点はコンパスの軸のように機能します。

基準点を使用すると、特定の基準点に基づいて、画像を回転、スケール、サイズ変更することができます。 参照ポイントは`northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`および`southeast`です。 例えば、中心の基準点を使用すると、グラフィックを中心に45°回転できます。 次の画像は、基準点の位置、グラフィック、グラフィックの`northWest`基準点から20°回転したグラフィック、およびグラフィックの`east`基準点から20°回転したグラフィックを示しています。

![参照点の画像](assets/wp_ref_points.png)

* A.基準点位置
* B. グラフィック
* C. グラフィックが`northWest`基準点から20°回転した
* D. グラフィックが`east`基準点から20°回転した

構文を次に示します。

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

デフォルト値はnoneです。 `inherit`の値は、`none`以外の場合、`s7:referencePoint`の値をページまたはグループレベルの先頭からすべての子に渡します。 `none`設定は、オブジェクトの基準点がなく、FXG座標系が使用されることを意味します。

>[!NOTE]
>
>基準点を使用し、操作後にオブジェクトが移動しないようにするには、操作した後でオブジェクトの x と y の値を更新します。

`s7:referencePoint`の値をグループ（またはパス、行の要素、または明示的な幅と高さの定義を持たない要素）と共に使用する場合、値はグループの累積境界ボックスに適用されます。 例えば、グループ内のすべてのオブジェクトのバウンディングボックスの左上のポイントがグループの`northWest`の基準点となり、右下のポイントが`southEast`の基準点となります。
