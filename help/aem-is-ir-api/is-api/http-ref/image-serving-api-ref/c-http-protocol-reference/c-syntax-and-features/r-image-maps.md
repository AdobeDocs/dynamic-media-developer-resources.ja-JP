---
description: ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは限定的です。
seo-description: ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは限定的です。
seo-title: 画像マップ
solution: Experience Manager
title: 画像マップ
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Image maps{#image-maps}

ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは限定的です。

ソース画像マップは、または `catalog::Map` コマンドを介してISに提供され、処理されたマップは、 `map=``req=map` コマンドを使用して検索されます。

画像マップは、1つ以上のHTML AREA要素で構成され、「&lt;」と「>」で適切に区切られています。 catalog::Mapを介して指定した場合、すべてのピクセル座標値は、元の画像解像度で、（変更されていない）ソース画像の左上隅を基準とした相対位置にあると見なされます。 コマンドを使用して指定した場合、座標値は、レイヤーの左上隅を基準としたレイヤー座標と見なされます( `map=` および `rotate=``extend=`の後ろ)。

>[!NOTE]
>
>現在、%座標は使用できないため、正しく処理されない場合があります。

ISは、各構成レイヤーのソース画像マップから、マップ座標に空間変換（拡大・縮小、回転など）を適用して合成画像マップを生成し、処理済みのレイヤーマップを適切なz順（前から後）、適切な位置にアセンブリします。

次の各コマンドは、 `req=map``catalog::Modifier` （要求内、カタログテンプレート経由、文字列内の）と組み合わせて提供する場合、画像マップの処理に使用します。

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

その他のコマンドはすべて、実際には無視されます。

リク `SHAPE` エストの処理中に、の属性 `COORDS` と属性を変更で `AREA` きる場合、その `req=map``AREA` 要素の他のすべての属性は変更されずに渡されます。 ほとんどの場合、 `SHAPE` 値をからに変更する `DEFAULT` (これによって `RECT` 属性が追加されます)か、 `COORDS``COORDS` 値を変更します。

処理中に空になる `AREA` 要素はすべて削除されます。 マップが関連付けられている場合は、そ `layer=comp` のマップは他のすべてのマップの後ろに配置されます。 データは、1つ以上のHTML `AREA` 要素からテキスト形式で返されます。 空の返信文字列は、指定したオブジェクトの画像マップが存在しないことを示します。

レイヤーの透明度は、マップの処理には考慮されません。 完全に透明なレイヤーには、画像マップを関連付けることができます。 部分的に透明なレイヤーのマップは、透明な領域にクリップされません。

## 関連項目 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01仕様](http://www.w3.org/TR/html401/)
