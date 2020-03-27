---
description: 画像サービングは、シンプルな透かしを埋め込む機能を実装します。
seo-description: 画像サービングは、シンプルな透かしを埋め込む機能を実装します。
seo-title: 透かし
solution: Experience Manager
title: 透かし
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 透かし{#watermarks}

画像サービングは、シンプルな透かしを埋め込む機能を実装します。

透かしは通常、半透明の画像ですが、テキストや、より複雑なレイヤー化された複合画像の場合があります。 すべてのビュー属性(、、、、 `wid=`)が適用された後、サーバーは返信画 `hei=`像の上に透か `align=`し `scl=`をレイ `bgc=`ヤーします。

透かしは、透かしの画像またはテ `attribute::Watermark` ンプレートを含む有効なカタログエントリをに設定することで有効にします。 を指定 `attribute::Watermark` したカタログに設定すると、サーバは要求URL内のカタログIDを参照するすべての画像要求に透かしを追加します。 を設 `default::Watermark` 定すると(初期設定のカタログで [!DNL default.ini])、カタログを参照しているかどうかに関係なく、すべての画像要求に透かしが適用されます。

サムネールの要求()およびScene7ビューアからの特定の要求に応答して返さ `req=tmb`れる画像には、透かしは適用されません。

## 拡大縮小と整列 {#section-89ef9e5926ae438abbd8e70332749b76}

透かしを指定すると、サーバはまず、透かしを適用する必要がある合成画像 **（ターゲット画像）を生成します（ビュー変換を適用する前に）。 次に、サーバは、他の画像(透かし画像 *)と同様に透かしの合成画像を生*&#x200B;成します。

標準の画像とは異な `sizeN=` り、透かし画像のlayer=0またはlayer=compに対して指定できます。 これにより、ターゲット画像を基準にして透かし画像を拡大・縮小できます。 指定し `sizeN=` なかった場合、透かし画像をターゲット画像と結合する際に、そのピクセルサイズが維持されます。

要求コマンド（など） `fmt=`や表示コマンド（など）は、を除 `wid=`き、透かしレコードでは無視されます `align=`。 `align=` を使用して、透かし画像をターゲット画像を基準とした透かし画像の相対位置に配置できます。 これにより、ターゲット画像の隅または端を基準にして透かしを配置できます。

拡大・縮小して整列した後、サーバは透かし画像に対して指定された値と値を使用して、透かし `blendMode=` 画像を `opac=` ターゲット画像に `layer=0` 重ね `layer=comp` ます。 最後に、対象画像に対して指定された要求および表示コマンドを適用し、返信画像を作成する。

透かし画像は、およびコマンドによって返信画像に追加された空白領域を超えることはあ `wid=` りません `hei=` 。

## 例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

一般的な透かしは、ロゴや著作権表示を含む単純なRGBA画像で構成されます。 に設定して、画像カタログ（または初期設定のカタログ）内にレコードを作成し、 `catalog::Id` で透かし画像 `watermark` ファイルを指定しま `catalog::Path`す。 透かしを拡大して、透かしの余白を少し残しながら、ビュー画像に合わせて（透かしを歪めずに）透かしを拡大し、不透明度を元の透かしの20%に減らすので、に設定し `catalog::Modifier` まし `sizeN=0.9,0.9&opac=20`た。 透かしをアクティブにす `attribute::Watermark` るには、透かしカタログエントリのID（この例では「透かし」）を設定します。 透かし効果を変えるために様々な選択を試し `blendMode=` てみたいと思うかもしれません

## 関連項目 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
