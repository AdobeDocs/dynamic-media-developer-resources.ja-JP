---
description: 画像サービングは、シンプルな視覚透かし処理機能を実装します。
solution: Experience Manager
title: 透かし
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---

# 透かし{#watermarks}

画像サービングは、シンプルな視覚透かし処理機能を実装します。

透かしは通常、半透明の画像ですが、テキストや、より複雑なレイヤー化された複合画像の場合があります。 すべてのビュー属性( `wid=` 、 `hei=` 、 `align=` 、 `scl=` 、 `bgc=` )が適用された後、サーバーは、返信画像の上に透かしを重ねます。

透かしは、`attribute::Watermark`を透かし画像またはテンプレートを含む有効なカタログエントリに設定することで有効になります。 名前付きカタログに`attribute::Watermark`が設定されている場合、サーバーは要求URLのカタログIDを参照するすべてのイメージ要求に透かしを追加します。 `default::Watermark`が（デフォルトのカタログ[!DNL default.ini]で）設定されている場合、透かしは、カタログを参照しているかどうかに関係なく、すべてのイメージリクエストに適用されます。

サムネールの要求(`req=tmb`)やDynamic Mediaのビューアからの要求に応じて返される画像には、透かしは適用されません。

## 拡大・縮小と整列 {#section-89ef9e5926ae438abbd8e70332749b76}

透かしを指定すると、サーバはまず透かしを適用する必要がある（ビュー変換を適用する前に）合成画像（*ターゲット画像*）を生成します。 次に、サーバは、他の画像（*透かし画像*）と同様に透かしの合成画像を生成する。

標準の画像とは異なり、`sizeN=`は、透かし画像のlayer=0またはlayer=compに指定できます。 これにより、対象画像を基準に透かし画像を拡大・縮小できます。 `sizeN=`を指定しない場合、透かし画像をターゲット画像とマージする際に、そのピクセルサイズが保持されます。

要求コマンド（`fmt=`など）と表示コマンド（`wid=`など）は、透かしレコードでは無視されますが、`align=`は除きます。 `align=` を使用して、透かし画像を、対象の画像を基準とした透かし画像を基準に配置できます。これにより、対象画像の隅または端を基準に透かしを配置できます。

拡大・整列後、サーバは透かし画像の`layer=0`または`layer=comp`に対して指定された`blendMode=`と`opac=`の値を使用して、対象画像に透かし画像を重ねます。 最後に、対象画像に対して指定された要求及び表示コマンドを適用し、返信画像を構築する。

透かし画像は、`wid=`および`hei=`コマンドによって返信画像に追加された空白領域を越えることはありません。

## 例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的な透かしは、ロゴや著作権表示を含む単純なRGBA画像で構成される場合があります。 `catalog::Id`を`watermark`に設定して、画像カタログ（またはデフォルトのカタログ）にレコードを作成し、`catalog::Path`に透かし画像ファイルを指定します。 透かしは、少し余白を残しながら（透かしをゆがめずに）表示画像に合わせて拡大し、不透明度を元の透かしの20%に減らしたいので、`catalog::Modifier`を`sizeN=0.9,0.9&opac=20`に設定します。 透かしを有効にするには、`attribute::Watermark`を透かしカタログエントリのID（この例では「透かし」）に設定します。 透かし効果を変えるには、様々な`blendMode=`選択を試してみるとよいでしょう。

## 関連項目 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
