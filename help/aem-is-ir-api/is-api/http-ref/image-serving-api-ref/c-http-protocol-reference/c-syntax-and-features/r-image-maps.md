---
description: は、HTML画像マップの使用を簡単にするメカニズムを提供します。 の JAVA ベースのビューアと Flash ベースのビューアも、画像マップを限定的にサポートしています。
solution: Experience Manager
title: 画像マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 画像マップ{#image-maps}

は、HTML画像マップの使用を簡単にするメカニズムを提供します。 の JAVA ベースのビューアと Flash ベースのビューアも、画像マップを限定的にサポートしています。

Source画像マップは、`catalog::Map` または `map=` コマンドを介して IS に提供され、処理済みのマップは `req=map` コマンドを使用して取得されます。

画像マップは、1 つ以上のHTML AREA 要素で構成され、適切に「&lt;」と「>」で区切られます。 catalog::Map を使用して指定した場合、すべてのピクセル座標の値は、元の画像の解像度にあり、（変更されていない）ソース画像の左上隅を基準にしていると見なされます。 `map=` コマンドを使用して指定した場合、座標値は、レイヤーの左上隅を基準としたレイヤー座標と見なされます（`rotate=` および `extend=` の後）。

>[!NOTE]
>
>% 座標は現在許可されていないため、正しく処理されない可能性があります。

IS は、各構成層のソース画像マップから合成画像マップを生成し、マップ座標に空間変換（スケーリングや回転など）を適用した後、適切な z オーダー（前面から背面）と適切な位置で処理済みの画層マップを組み立てます。

次のコマンドは、`req=map` と組み合わせて（リクエストで直接、カタログテンプレートを使用して、または文字列で）指定された場合に、画像マップの処理で考慮さ `catalog::Modifier` ます。

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

その他のコマンドは事実上無視されます。

`SHAPE` の `COORDS` 属性と `AREA` 属性は、`req=map` リクエストの処理中に変更される可能性があり、`AREA` 要素のその他すべての属性は変更されずに渡されます。 ほとんどの場合、`SHAPE` 値を `DEFAULT` から `RECT` に変更するか（これにより `COORDS` 属性も追加されます）、`COORDS` 値を変更する必要があります。

処理中に空になった `AREA` 要素は完全に削除されます。 マップが `layer=comp` に関連付けられている場合、そのマップは他のすべてのマップの背後に配置されます。 データは、1 つ以上のHTML `AREA` 要素として、テキスト形式で返されます。 空の返信文字列は、指定したオブジェクトの画像マップが存在しないことを示します。

レイヤーの透明度はマップ処理には考慮されません。 完全に透明なレイヤーには、画像マップを関連付けることができます。 部分的に透明なレイヤーのマップは、透明領域にクリップされません。

## 関連項目 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 仕様 ](https://www.w3.org/TR/html401/)
