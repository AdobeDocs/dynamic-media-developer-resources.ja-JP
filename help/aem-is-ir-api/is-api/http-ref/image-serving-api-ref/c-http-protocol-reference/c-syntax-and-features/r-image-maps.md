---
description: ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは制限されています。
solution: Experience Manager
title: 画像マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 画像マップ{#image-maps}

ISは、HTML画像マップの使用を簡略化するメカニズムを提供します。 ISのJAVAベースおよびFlashベースのビューアでも、画像マップのサポートは制限されています。

ソース画像マップは、`catalog::Map`または`map=`コマンドを使用してISに提供され、処理されたマップは`req=map`コマンドを使用して取得されます。

画像マップは、1つ以上のHTML AREA要素で構成され、「&lt;」と「>」で適切に区切られます。 catalog::Mapを使用して指定した場合、すべてのピクセル座標値は元の画像解像度で、（変更されていない）ソース画像の左上隅を基準とした相対値と見なされます。 `map=`コマンドで指定した場合、座標値は、レイヤーの左上隅を基準としたレイヤー座標と見なされます（`rotate=`および`extend=`の後）。

>[!NOTE]
>
>%座標は現時点では許可されず、正しく処理されない場合があります。

ISは、各構成レイヤのソース画像マップから、マップ座標に空間変換（スケーリングや回転など）を適用し、処理されたレイヤマップを適切なz順（前後）で適切な位置に組み立てて合成画像マップを生成する。

`req=map`と組み合わせて（リクエスト内、カタログテンプレート経由、または`catalog::Modifier`文字列内で）画像マップを処理する場合、以下のコマンドを考慮します。

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

その他のコマンドは、事実上無視されます。

`AREA`の`SHAPE`属性と`COORDS`属性は、`req=map`リクエストの処理中に変更できます。`AREA`要素のその他すべての属性は、変更されずに渡されます。 ほとんどの場合、`SHAPE`値を`DEFAULT`から`RECT`に変更するか（`COORDS`属性も追加します）、`COORDS`値を変更します。

処理中に空になる`AREA`要素はすべて削除されます。 マップが`layer=comp`に関連付けられている場合は、他のすべてのマップの後に配置されます。 データは、1つ以上のHTML `AREA`要素としてテキスト形式で返されます。 空の返信文字列は、指定したオブジェクトの画像マップが存在しないことを示します。

マップ処理では、画層の透明度は考慮されません。 完全に透明なレイヤーには、画像マップが関連付けられている場合もあります。 部分的に透明なレイヤーのマップは、透明な領域にクリップされません。

## 関連項目 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) 、 [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)、 [HTML 4.01仕様](https://www.w3.org/TR/html401/)
