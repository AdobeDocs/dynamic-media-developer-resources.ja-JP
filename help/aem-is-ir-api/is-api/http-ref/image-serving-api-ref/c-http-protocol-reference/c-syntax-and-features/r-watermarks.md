---
description: 画像サービングは、シンプルな視覚的な透かし機能を実装しています。
solution: Experience Manager
title: 透かし
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
TQID: 'https://experienceleague.adobe.com/5gqAaM5kFHj67LxcMVGeEU2uus6mA-BT9kCewY1cZOw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# 透かし{#watermarks}

画像サービングは、シンプルな視覚的な透かし機能を実装しています。

通常、透かしは半透明の画像ですが、テキスト画像や、より複雑でレイヤー化された合成画像を使用する場合があります。 サーバーは、すべてのビュー属性（`wid=`、`hei=`、`align=`、`scl=`、`bgc=`）が適用された後、返信画像に透かしをレイヤーします。

透かしは、透かし画像またはテンプレートを含む有効なカタログエントリに`attribute::Watermark`を設定することで有効になります。 `attribute::Watermark`が名前付きカタログに設定されている場合、サーバーは、リクエスト URLでカタログ IDを参照するすべての画像リクエストに透かしを追加します。 `default::Watermark`が設定されている場合（デフォルトのカタログでは[!DNL default.ini]）、カタログを参照しているかどうかに関係なく、すべてのイメージリクエストに透かしが適用されます。

サムネールリクエスト（`req=tmb`）およびDynamic Media ビューアからの特定のリクエストに応じて返された画像には、透かしが適用されません。

## 拡大・縮小と調整 {#section-89ef9e5926ae438abbd8e70332749b76}

透かしを指定すると、サーバーは最初に、透かしを適用する必要がある合成画像（*ターゲット画像*）を（ビューを適用する前に）生成します。 次に、サーバーは、他の画像（*透かし画像*）と同様に、透かしの合成画像を生成します。

標準的な画像とは異なり、透かし画像のlayer=0またはlayer=compに`sizeN=`を指定できます。 これにより、ターゲット画像に対して透かし画像を拡大・縮小できます。 `sizeN=`が指定されていない場合、透かし画像はターゲット画像と結合されるときにピクセルサイズを保持します。

`fmt=`などの要求コマンドと`wid=`などの表示コマンドは、`align=`を除き、透かしレコードでは無視されます。 `align=`を使用して、ターゲット画像に対する透かし画像を基準とした透かし画像を配置できます。 これにより、ターゲット画像のコーナーまたはエッジに対して透かしを配置できます。

拡大縮小と整列の後、サーバーは、透かし画像の`layer=0`または`layer=comp`に指定された`blendMode=`と`opac=`の値を使用して、ターゲット画像に透かし画像を重ねます。 最後に、ターゲット画像に対して指定されたリクエストコマンドおよびビューコマンドを適用して、返信画像を作成する。

透かし画像は、`wid=`および`hei=` コマンドによって返信画像に追加された空白を超えることはありません。

## 例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

一般的な透かしは、ロゴや著作権通知を含むシンプルなRGBA画像で構成されます。 `catalog::Id`が`watermark`に設定された画像カタログ（またはデフォルトのカタログ）にレコードを作成し、`catalog::Path`に透かし画像ファイルを指定します。 透かしをビュー画像に合わせて（透かしを歪ませずに）引き伸ばし、不透明度を元の透かしの20%に減らします。そのため、`catalog::Modifier`を`sizeN=0.9,0.9&opac=20`に設定します。 透かしを有効にするには、この例では、`attribute::Watermark`を透かしカタログエントリのID 「透かし」に設定します。 様々な透かし効果を得るために、様々な`blendMode=`の選択肢を試してみるといいかもしれません。

## 関連項目 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
