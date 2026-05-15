---
description: ISは、HTML画像マップの使用を簡略化する仕組みを提供します。 ISのJAVA ベースおよびFlash ベースのビューアには、画像マップのサポートが限定的です。
solution: Experience Manager
title: 画像マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
TQID: 'https://experienceleague.adobe.com/r0AiVRiFWvxKwq-80xpo-G4gZZDCRE6WjciJpiz9V-U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 389
ht-degree: 0%

---

# 画像マップ{#image-maps}

ISは、HTML画像マップの使用を簡略化する仕組みを提供します。 ISのJAVA ベースおよびFlash ベースのビューアには、画像マップのサポートが限定的です。

Source画像マップは、`catalog::Map`または`map=` コマンドを使用してISに提供され、処理されたマップは`req=map` コマンドを使用して取得されます。

画像マップは、1つ以上のHTML AREA要素で構成され、「&lt;」と「>」で適切に区切られます。 catalog::Mapによって提供される場合、すべてのピクセル座標の値は、元の画像解像度で、（変更されていない）ソース画像の左上隅を基準としたものとみなされます。 `map=` コマンドを使用して指定した場合、座標値は、レイヤーの左上隅（`rotate=`および`extend=`以降）を基準としたレイヤー座標と見なされます。

>[!NOTE]
>
>%個の組み合わせは現在許可されておらず、誤って処理される可能性があります。

ISは、各構成層の元画像マップから合成画像マップを生成し、空間変換（スケーリングや回転など）をマップ座標に適用し、処理されたレイヤーマップを適切なz次（前から後へ）に組み立て、適切な位置に配置する。

次のコマンドは、`req=map`と組み合わせて指定する場合（リクエストで直接指定するか、カタログテンプレートを使用するか、`catalog::Modifier`文字列で指定する場合）に、画像マップ処理に使用されます。

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

その他のコマンドはすべて効果的に無視されます。

`AREA`の`SHAPE`属性と`COORDS`属性は、`req=map`要求の処理中に変更される可能性がありますが、`AREA`要素の他のすべての属性は変更なしで渡されます。 ほとんどの場合、これには`SHAPE`の値を`DEFAULT`から`RECT`に変更するか（`COORDS`属性も追加されます）、`COORDS`の値を変更することが含まれます。

処理中に空になった`AREA`要素はすべて完全に削除されます。 マップが`layer=comp`に関連付けられている場合、そのマップは他のすべてのマップの後ろに配置されます。 データは、1つ以上のHTML `AREA`要素としてテキスト形式で返されます。 空の返信文字列は、指定されたオブジェクトに画像マップが存在しないことを示します。

レイヤーの透明度はマップ処理では考慮されません。 完全に透明なレイヤーでも、画像マップを関連付けることができます。 部分的に透明なレイヤーのマップは、透明領域にクリップされません。

## 関連項目 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06)、[&#x200B; カタログ：:Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)、[HTML 4.01の仕様](https://www.w3.org/TR/html401/)
