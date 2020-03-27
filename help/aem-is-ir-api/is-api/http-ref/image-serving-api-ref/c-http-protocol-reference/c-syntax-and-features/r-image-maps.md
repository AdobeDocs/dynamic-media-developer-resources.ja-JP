---
description: ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは限定的です。
seo-description: ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは限定的です。
seo-title: 画像マップ
solution: Experience Manager
title: 画像マップ
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Image maps{#image-maps}

ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは限定的です。

ソース画像マップは、コマンドを介してまたは `catalog::Map` コマンドを使用し `map=` てISに提供され、処理されたマップは、コマンドを使用して取得 `req=map` されます。

画像マップは、1つ以上のHTML AREA要素で構成され、「&lt;」と「>」で適切に区切られます。 catalog::Mapを使用して指定した場合、すべてのピクセル座標値は元の画像解像度で、（変更されていない）ソース画像の左上隅を基準にした相対値と見なされます。 コマンドを使用 `map=` して指定した場合、座標値は、レイヤーの左上隅を基準としたレイヤー座標と見なさ `rotate=` れま `extend=`す。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>%座標は現時点では許可されておらず、正しく処理されない場合があります。

ISは、各構成レイヤーのソース画像マップから、空間変換（スケーリングや回転など）をマップ座標に適用し、処理済みのレイヤーマップを適切なz順序（前から後）および適切な位置にアセンブリして、合成画像マップを生成します。

次のコマンドは、（要求内、カタログテンプレート経由、または文字列内で） `req=map` と組み合わせて提供される場合、画像マップの処理に使用さ `catalog::Modifier` れます。

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

その他のコマンドはすべて、事実上無視されます。

リクエスト `SHAPE` の処理中に、お `COORDS` よびの属性を変更でき `AREA` ます。その他の要素の属性は、変更せず `req=map``AREA` にすべて渡されます。 ほとんどの場合、値をからに変 `SHAPE` 更する `DEFAULT` (これに `RECT` よって属性が追加されます)か、値 `COORDS` を変更し `COORDS` ます。

処理中 `AREA` に空になった要素はすべて削除されます。 マップが関連付けられている場合は、そ `layer=comp` のマップは他のすべてのマップの後ろに配置されます。 データは、1つ以上のHTML要素からテキスト形式で返さ `AREA` れます。 空の返信文字列は、指定したオブジェクトの画像マップが存在しないことを示します。

レイヤーの透明度は、マップの処理には考慮されません。 完全に透明なレイヤーには、画像マップを関連付けることができます。 部分的に透明なレイヤーのマップは、透明な領域にクリップされません。

## 関連項目 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01仕様](http://www.w3.org/TR/html401/)
