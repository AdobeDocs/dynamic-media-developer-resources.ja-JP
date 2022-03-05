---
description: IS は、画像画像マップの使用を簡略化するHTMLを提供します。 IS の JAVA ベースおよびFlashベースのビューアでも、画像マップのサポートは制限されています。
solution: Experience Manager
title: 画像マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 画像マップ{#image-maps}

IS は、画像画像マップの使用を簡略化するHTMLを提供します。 IS の JAVA ベースおよびFlashベースのビューアでも、画像マップのサポートは制限されています。

ソース画像マップは、 `catalog::Map` または `map=` コマンドを実行すると、処理されたマップは `req=map` コマンドを使用します。

画像マップは、1 つ以上のHTMLAREA 要素で構成され、「&lt;」と「>」で適切に区切られます。 catalog::Map を使用して指定した場合、すべてのピクセル座標値は元の画像解像度で、（未変更の）ソース画像の左上隅を基準とした相対値と見なされます。 を介して提供される場合 `map=` の場合、座標値は画層の左上隅を基準とした画層座標と見なされます ( `rotate=` および `extend=`) をクリックします。

>[!NOTE]
>
>現在、%座標は許可されていないので、正しく処理されない場合があります。

IS は、各構成レイヤのソースイメージマップから、マップ座標に空間変換（拡大・縮小、回転など）を適用し、処理されたレイヤマップを適切な z 順（前から後）に、適切な位置に組み立てて合成イメージマップを生成する。

画像マップの処理で、 `req=map` ( リクエスト内、カタログテンプレート経由、または `catalog::Modifier` 文字列 ):

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

この `SHAPE` および `COORDS` の属性 `AREA` 処理中に変更される可能性がある `req=map` リクエスト、 `AREA` 要素は変更されずに渡されます。 ほとんどの場合、これには `SHAPE` 値 `DEFAULT` から `RECT` ( この場合、 `COORDS` 属性 )、または `COORDS` 値。

任意 `AREA` 処理中に空になる要素は完全に削除されます。 マップが `layer=comp` 他の全ての地図の後ろに置かれています データは、1 つ以上のHTML `AREA` 要素。 空の返信文字列は、指定したオブジェクトに画像マップが存在しないことを示します。

マップの処理では、レイヤの透明度は考慮されません。 完全に透明なレイヤーには、画像マップが関連付けられた状態を保つことができます。 部分的に透明なレイヤのマップは、透明な領域にクリップされません。

## 関連項目 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML4.01 の仕様](https://www.w3.org/TR/html401/)
