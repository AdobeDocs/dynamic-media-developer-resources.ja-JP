---
description: ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースのビューアおよびFlashベースのビューアでも、画像マップのサポートは限定的です。
seo-description: ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースのビューアおよびFlashベースのビューアでも、画像マップのサポートは限定的です。
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


# 画像マップ{#image-maps}

ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースのビューアおよびFlashベースのビューアでも、画像マップのサポートは限定的です。

ソース画像マップは、`catalog::Map`または`map=`コマンドを介してISに提供され、処理されたマップは、`req=map`コマンドを使用して取得されます。

画像マップは、1つ以上のHTML AREA要素で構成され、「&lt;」と「>」で適切に区切られています。 catalog::Mapを介して指定した場合、すべてのピクセル座標値は、元の画像解像度で、（変更されていない）ソース画像の左上隅を基準とした相対位置にあると見なされます。 `map=`コマンドを使用して指定した場合、座標値は、レイヤーの左上隅を基準としたレイヤー座標と見なされます（`rotate=`と`extend=`の後）。

>[!NOTE]
>
>現在、%座標は使用できないため、正しく処理されない場合があります。

ISは、各構成レイヤーのソース画像マップから、マップ座標に空間変換（拡大・縮小、回転など）を適用して合成画像マップを生成し、処理済みのレイヤーマップを適切なz順（前から後）、適切な位置にアセンブリします。

次のコマンドは、`req=map`と組み合わせて（要求内で直接、カタログテンプレート経由、または`catalog::Modifier`文字列内で）提供する場合の画像マップ処理に使用します。

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

`AREA`の`SHAPE`属性と`COORDS`属性は、`req=map`要求の処理中に変更できます。`AREA`要素の他のすべての属性は、変更せずに渡されます。 ほとんどの場合、`SHAPE`値を`DEFAULT`から`RECT`に変更するか（これも`COORDS`属性を追加します）、`COORDS`値を変更します。

処理中に空になる`AREA`要素はすべて削除されます。 マップが`layer=comp`に関連付けられている場合は、他のすべてのマップの背後に配置されます。 データは、1つ以上のHTML `AREA`要素としてテキスト形式で返されます。 空の返信文字列は、指定したオブジェクトの画像マップが存在しないことを示します。

レイヤーの透明度は、マップの処理には考慮されません。 完全に透明なレイヤーには、画像マップを関連付けることができます。 部分的に透明なレイヤーのマップは、透明な領域にクリップされません。

## 関連項目 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01仕様](http://www.w3.org/TR/html401/)
