---
description: 画像サービングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。
seo-description: 画像サービングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。
seo-title: 画像サービングのカラーマネジメント
solution: Experience Manager
title: 画像サービングのカラーマネジメント
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 画像サービングのカラーマネジメント{#image-serving-color-management}

画像サービングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。

## 初期設定のカラースペース {#section-8cfe60808bce49968091995e4e521dba}

各画像カタログ（および初期設定のカタログ）では、このカタログの初期設定のカラースペースを構成するICCプロファイルのセットを定義できます。1つの入力プロファイルと1つの出力プロファイルは、グレースケール、RGB、CMYKデータ用です。 See ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, and ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## 入力カラースペース {#section-9f08e2c1b6aa4fe4815be174972c1944}

ソース画像には、ICCプロファイルが埋め込まれ、入力カラースペースが定義される場合があります。 ソース画像にプロファイルが埋め込まれていない場合は、ソ `attribute::IccProfileSrc*` ース画像のピクセルタイプに対応する適用可能な画像カタログのプロファイルが使用されます。 この属性が画像カタログで定義されていない場合、が使 `attribute::IccProfile*` 用されます。 カタログ属性も定義されていない場合、画像はカラーマネジメントされず、単純な変換のみが適用されます。

## 出力カラースペース {#section-b517bca622b64dcfa7defba6035d0716}

要求の最終的なイメージ結果のカラースペースは、コマンドで定義さ `icc=` れます。 を指 `icc=` 定しない場合、出力画像のピクセルタイプに対応する（要求のメインカタログからの）デフォルトの出力カラースペースが出力カラースペースとして使用されます。 メインまたは初期設定のカタログに出力プロファイルが定義されていない場合、およびベースレイヤーが、出力ピクセルの種類と一致する埋め込みプロファイルを持つ画像の場合、そのプロファイルが出力カラースペースに使用されます。 そうしないと、出力カラースペースは未定義のままになり、ピクセルタイプ間の変換時には純粋なカラー変換のみが適用され、出力画像にはカラープロファイルを埋め込めません。

ネストされた/埋め込まれた画像サービング要求の出力カラースペースは、常に、外側の埋め込み要求の出力カラースペースと同じです。

## べた塗り {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

、、またはRTFコマ `color=`ン `bgcolor=``\iscolortbl` ドで指定したカラー値は、入力カラースペースにカラー値にサフィックス「S」が含まれている場合は関連付けられ、それ以外の場合は出力カラースペースに関連付けられます。 またはRTFコマンドで指 `bgc=` 定したカラー値と、 `\colortbl` 常に `\cmykcolortbl` 対応するデフォルトまたは実際の出力カラースペースに関連付けられます。

>[!NOTE]
>
>現時点では、 `bgc=``bgc=``bgc=` はカラーマネジメントに完全に関与しません。で指定した場合、「S」サフィックスは無視され、で指定したカラー値のピクセルタイプが出力画像のピクセルタイプと異なる場合、純粋な変換が適用されます。 それ以外の場合 `bgc=` は、は実際の出力カラースペースに関連付けられます。

## ネストされたリクエストと埋め込まれたリクエスト {#section-bdda638c31504f26a77e51ebb1ea6e3b}

入れ子にされたIS要求と埋め込まれたIR要求の出力カラースペースは、入れ子にされた要求で明示的な出力カラースペースが指定されていない限り、自動的に最も外側の要求の出力カラースペースに設定されま `icc=`す。 さらに、ネスト/埋め込みリクエストも、最も外側のリクエストのメインカタログからデフォルトの出力カラースペースを継承し、べた塗りの値の処理を一貫させます。

## カラースペースの変換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

通常、画像サービングは、処理中に色の変換を遅らせようとします。 画像のすべてのレイヤーのカラースペースが同じである場合、出力カラースペースへの変換は、結合して最終的に拡大縮小した後に行われます。 複数のレイヤーカラースペースが含まれる場合、各レイヤーは結合前に出力カラースペースに変換されます。

>[!NOTE]
>
>、、、およ `op_brightness=`びの各コ `op_colorbalance=`マンド `op_colorize=`は、RGB `op_contrast=`の `op_hue=`操作 `op_saturation=` を行います。 これらの操作では、レイヤーのカラースペースにRGBピクセルタイプが含まれている場合にのみ、カラーの忠実度が維持されます。 RGB以外の場合、データは純粋なカラー変換を使用してRGBに変換され、結果の色の忠実度は制限されます。 このようなレイヤーのレイヤーカラースペースは、不確定と見なされます。

カラー変換オプションは、またはを `icc=` 指定しない場 `icc=` 合は、、、およびとと共に `attribute::IccRenderIntent`提供さ `attribute::IccBlackPointCompensation`れま `attribute::IccDither`す。

## カラープロファイルの埋め込み {#section-261ebbae5ce046589a776ca972380052}

出力カラースペースのICCカラープロファイルがある場合は、を指定して応答画像に埋め込むことができま `iccEmbed=`す。

## ICCプロファイルの管理 {#section-eb210e4b44e64e2c8b80ee59216c5555}

サーバが使用するすべてのカラープロファイルは、ICC仕様に準拠している必要があります。 ICCプロファイルファイルは、通常、ファ [!DNL .icc] イルのサ [!DNL .icm] フィックスまたはファイル名を持ち、画像データファイルと共に配置されます。

出力プロファイルはコマンド内のファイルパス/名前で指定できますが、初期設定のカタログまたは画像カタログのICCプロファイルマップにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカット識別子( `icc=``icc::Name`)を使用することをお勧めします。

とで参照されるすべてのICCプ `catalog::IccProfile` ロファイルは、 `attribute::IccProfile*` 画像または初期設定のカタログのICCプロファイルマップに登録する必要があります。

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされています。

## 付属のICCカラープロファイル {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

画像サービングでは、ほとんどの標準Adobe ICCプロファイルが初期設定の画像カタログに含まれています。 これらのプロファイルは、共通名（Photoshopで表示されるような名前）またはやや短い識別子を使用してアクセスできます。 次の表に、すべての標準ICCプロファイルを示します。 コマンド内のプロファイルを共通名 `icc=` で参照する場合、スペースは、としてエンコードする必要がありま `%20`す。

デフォルトのカタログまたは特定の画像カタログのいずれかに、追加のプロファイルを標準プロファイルに追加できます。 詳しくは、 [ICCプロファイルマップリファレンスを参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) 。

>[!NOTE]
>
>次の表は、ダイナミック *メディアハイブリッド* （実行モードで実行） `dynamicmedia` のみに適用されます。

|識別子|共通名|ファイル名||—|—|—||**RGB**|||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB`|CIE RGB|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto`|ProPhoto RGB|ProPhoto.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm||`WideGamutRGB`|広色域RGB|WideGamatRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002新聞|JapanColor2002新聞.icc||`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc||`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`NewsprintSNAP2007`|USニュースプリント(SNAP 2007)|USNewsprintSNAP2007.icc||`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5初期設定のCMYK|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|米国Sheetfed Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|米国Sheetfed Uncoated v2|USSheetfedUncoated.icc||`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc||`WebCoated`|米国Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`WebCoatedGrade3`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc||`WebCoatedGrade5`|Web Coated SWOP 2006 Grade 5用紙|WebCoatedSWOP2006Grade5.icc||`WebUncoated`|米国Web Uncoated v2|USWebUncoated.icc|

次の表は、 *Dynamic Media Classic(Scene7)画像サービングおよびダイナミッ* クメディア *(実行モード*`dynamicmedia_scene7` で実行中)に適用されます。

|識別子|共通名|ファイル名||—|—|—||**RGB**|||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB|CIE RGB`|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm||`WideGamutRGB`|広色域RGB|WideGamatRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002新聞|JapanColor2002新聞.icc||`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc||`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5初期設定のCMYK|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|米国Sheetfed Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|米国Sheetfed Uncoated v2|USSheetfedUncoated.icc||`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc||`US Newsprint (SNAP 2007)`|USニュースプリント(SNAP 2007)|USNewsprintSNAP2007.icc||`WebCoated`|米国Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc||`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006 Grade 5用紙|WebCoatedSWOP2006Grade5.icc||`WebUncoated`|米国Web Uncoated v2|USWebUncoated.icc|

## 関連項目 {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),,:IccProfile [*, attribute:IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[ *, SrcProfile*,SrcProfile*,SrcProfileAttribute:IccRender Intent Render, Black Point Poic Ponent Pon:profile, ICC Map, ICC Reference color=, *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
