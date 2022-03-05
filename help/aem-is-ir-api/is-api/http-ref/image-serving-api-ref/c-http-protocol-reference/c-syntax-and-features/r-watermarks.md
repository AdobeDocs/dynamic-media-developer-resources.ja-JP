---
description: 画像サービングは、シンプルな視覚的透かし処理機能を実装します。
solution: Experience Manager
title: 透かし
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# 透かし{#watermarks}

画像サービングは、シンプルな視覚的透かし処理機能を実装します。

透かしは通常、半透明の画像ですが、テキストや、より複雑なレイヤー化された複合画像の場合があります。 サーバは、すべての表示属性 ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) が適用されています。

透かしは、 `attribute::Watermark` 透かし画像またはテンプレートを含む有効なカタログエントリに追加します。 If `attribute::Watermark` が名前付きカタログに設定されている場合、サーバーは要求 URL 内のカタログ ID を参照するすべてのイメージ要求に透かしを追加します。 If `default::Watermark` が設定されている場合 ( デフォルトのカタログでは [!DNL default.ini]) の場合、カタログを参照しているかどうかに関係なく、すべてのイメージリクエストに透かしが適用されます。

サムネール要求 ( `req=tmb`) や、Dynamic Mediaビューアからの特定の要求に対して実行されます。

## 拡大・縮小と整列 {#section-89ef9e5926ae438abbd8e70332749b76}

透かしを指定すると、サーバはまず合成画像 ( *ターゲット画像*) をクリックし、透かしを適用する必要がある（ビュー変換を適用する前に）をクリックします。 次に、サーバは、他の画像 ( *透かし画像*) をクリックします。

標準画像とは異なり、 `sizeN=` は、透かし画像の layer=0 または layer=comp に指定できます。 これにより、ターゲット画像を基準に透かし画像を拡大・縮小できます。 If `sizeN=` を指定しない場合、透かし画像をターゲット画像と結合する際に、透かし画像のピクセルサイズが保持されます。

要求コマンド ( `fmt=`) と表示コマンド ( `wid=`) は透かしレコードで無視されます ( ただし、 `align=`. `align=` を使用して、透かし画像を、対象の画像を基準とした透かし画像を基準に配置できます。 これにより、ターゲット画像の角または端を基準に透かしを配置できます。

拡大・整列後、サーバは、 `blendMode=` および `opac=` 指定された値 `layer=0` または `layer=comp` 透かし画像の。 最後に、対象画像に対して指定された要求および表示コマンドを適用して、返信画像を作成します。

透かし画像は、返信画像に追加された空白領域を越えて、 `wid=` および `hei=` コマンド

## 例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的な透かしは、ロゴや著作権情報を含む単純な RGBA 画像で構成される場合があります。 画像カタログ（またはデフォルトのカタログ）に、 `catalog::Id` に設定 `watermark` 透かし画像ファイルを指定するには、 `catalog::Path`. 透かしを拡大し、透かしを少し余分な余白を残しながら（透かしをゆがめずに）表示画像に合わせて表示し、透かしを元の透かしの 20%に減らしたいので、 `catalog::Modifier` から `sizeN=0.9,0.9&opac=20`. 透かしを有効にするには、 `attribute::Watermark` 透かしカタログエントリの id に、この例では「watermark」と入力します。 別のものを試してみたいと思うかもしれません `blendMode=` 透かし効果を異にする選択肢

## 関連項目 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
