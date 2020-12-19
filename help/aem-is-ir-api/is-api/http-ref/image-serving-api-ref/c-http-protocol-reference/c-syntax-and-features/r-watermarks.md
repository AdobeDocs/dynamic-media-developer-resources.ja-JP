---
description: 画像サービングには、シンプルな視覚的な透かし機能が実装されています。
seo-description: 画像サービングには、シンプルな視覚的な透かし機能が実装されています。
seo-title: 透かし
solution: Experience Manager
title: 透かし
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 1%

---


# 透かし{#watermarks}

画像サービングには、シンプルな視覚的な透かし機能が実装されています。

透かしは通常、半透明の画像ですが、テキストや、より複雑なレイヤー化された複合画像の場合があります。 すべての表示属性(`wid=`、`hei=`、`align=`、`scl=`、`bgc=`)が適用された後、サーバーは、返信画像に透かしを重ねます。

透かしは、`attribute::Watermark`を有効なカタログエントリに設定すると有効になります。このカタログエントリには透かしの画像またはテンプレートが含まれます。 名前付きカタログに`attribute::Watermark`が設定されている場合、サーバーは要求URL内のカタログIDを参照するすべての画像要求に透かしを追加します。 `default::Watermark`が設定されている場合（初期設定のカタログ[!DNL default.ini]内）、カタログを参照しているかどうかに関係なく、すべての画像要求に透かしが適用されます。

サムネールの要求(`req=tmb`)およびScene7の閲覧者からの特定の要求に応じて返される画像には、透かしは適用されません。

## スケールと位置合わせ{#section-89ef9e5926ae438abbd8e70332749b76}

透かしを指定すると、サーバは、まず、透かしを適用する必要のある合成画像(*ターゲット画像*)を生成します(表示変換を適用する前に)。 次に、サーバは、他の画像（*透かし画像*）と同様に、透かし用の合成画像を生成する。

標準の画像とは異なり、`sizeN=`は、透かし画像のlayer=0またはlayer=compに対して指定できます。 これにより、透かし画像をターゲット画像を基準にして拡大・縮小できます。 `sizeN=`を指定しない場合、透かし画像との結合時に、ターゲット画像のピクセルサイズが保持されます。

要求コマンド（`fmt=`など）と表示コマンド（`wid=`など）は、`align=`を除き、透かしレコードでは無視されます。 `align=` は、透かし画像を透かしターゲットを基準にして、透かし画像を配置する場合に使用します。これにより、透かしをターゲット画像の隅または端を基準にして配置できます。

拡大・縮小および整列の後、サーバは、透かし画像の`layer=0`または`layer=comp`に対して指定された`blendMode=`値と`opac=`値を使用して、ターゲット画像の上に透かし画像を配置します。 最後に、ターゲット画像に対して指定された要求コマンド及び表示コマンドを適用し、返信画像を作成する。

透かしの画像は、`wid=`および`hei=`コマンドによって返信画像に追加された空白領域を越えることはありません。

## 例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

標準的な透かしは、ロゴや著作権表示を含む単純なRGBA画像で構成される場合があります。 ここでは、`catalog::Id`を`watermark`に設定して画像カタログ（または初期設定のカタログ）にレコードを作成し、`catalog::Path`に透かし画像ファイルを指定します。 透かしの余白を少し残したまま、表示の画像に合わせて（透かしをゆがめずに）透かしを拡大し、不透明度を元の透かしの20%に減らしたいので、`catalog::Modifier`を`sizeN=0.9,0.9&opac=20`に設定します。 透かしを有効にするには、`attribute::Watermark`を透かしカタログエントリのID（この例では「watermark」）に設定します。 異なる透かし効果を得るために、`blendMode=`の異なる選択を試すことができます。

## 関連項目 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
