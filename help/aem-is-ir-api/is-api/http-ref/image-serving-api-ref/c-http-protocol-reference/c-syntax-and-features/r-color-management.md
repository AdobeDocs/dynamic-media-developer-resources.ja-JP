---
title: 画像サービングのカラーマネジメント
description: 画像サービングは、ICC(International Color Consortium) の仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 2%

---

# 画像サービングのカラーマネジメント{#image-serving-color-management}

画像サービングは、ICC(International Color Consortium) の仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。

## 初期設定のカラースペース {#section-8cfe60808bce49968091995e4e521dba}

各画像カタログ（およびデフォルトのカタログ）は、このカタログのデフォルトカラースペースを構成する ICC プロファイルのセットを定義できます。1 つの入力プロファイルと 1 つの出力プロファイルで、それぞれグレースケール、RGB、CMYK データを定義します。 詳しくは、
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## 入力カラースペース {#section-9f08e2c1b6aa4fe4815be174972c1944}

ソース画像は、ICC プロファイルを埋め込んで、入力カラースペースを定義できます。 ソース画像にプロファイルが埋め込まれていない場合、 `attribute::IccProfileSrc*` ソース画像のピクセルタイプに対応する適用可能な画像カタログのを使用する。 画像カタログでこの属性が定義されていない場合、 `attribute::IccProfile*` が使用されます。 そのカタログ属性も定義されていない場合、画像は色管理されず、単純な変換のみが適用されます。

## 出力カラースペース {#section-b517bca622b64dcfa7defba6035d0716}

リクエストの最終的なイメージ結果のカラースペースは、 `icc=` コマンドを使用します。 次の場合 `icc=` が指定されていない場合、出力画像のピクセルタイプに対応する（リクエストのメインカタログからの）デフォルトの出力カラースペースが出力カラースペースとして使用されます。 メインまたはデフォルトのカタログで出力プロファイルが定義されていない場合で、ベースレイヤーが出力ピクセルタイプに一致する埋め込みプロファイルを持つ画像の場合、そのプロファイルが出力カラースペースに使用されます。 そうしないと、出力カラースペースは未定義のままになります。ピクセルタイプ間での変換時に適用されるのは単純なカラー変換のみで、出力画像にはカラープロファイルを埋め込むことができません。

ネストされた/埋め込み画像サービング要求の出力カラースペースは、常に、外部の埋め込み要求の出力カラースペースと同じです。

## べた塗り {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

で指定したカラー値 `color=`, `bgcolor=`、または RTF コマンド `\iscolortbl` 色の値にサフィックス「S」が含まれる場合は入力カラースペースに関連付け、それ以外の場合は出力カラースペースに関連付けます。 で指定したカラー値 `bgc=` または RTF コマンド `\colortbl` および `\cmykcolortbl` は常に、対応するデフォルトまたは実際の出力カラースペースに関連付けられます。

>[!NOTE]
>
>この時 `bgc=` カラーマネジメントに完全に参加していない — 「S」サフィックスは、 `bgc=`を指定し、 `bgc=` は、出力画像のピクセルタイプとは異なります。 それ以外の場合は、 `bgc=` は、実際の出力カラースペースに関連付けられています。

## ネストされたリクエストと埋め込まれたリクエスト {#section-bdda638c31504f26a77e51ebb1ea6e3b}

ネストされた IS 要求と埋め込み IR 要求の出力カラースペースは、ネストされた要求で `icc=`. また、ネストされた/埋め込みリクエストも、最も外側のリクエストのメインカタログからデフォルトの出力カラースペースを継承するので、べた塗りの値を一貫して処理できます。

## カラースペースの変換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

通常、画像サービングは、処理中に色の変換を遅らせようとします。 画像のすべてのレイヤーのカラースペースが同じ場合は、マージして最終的に拡大・縮小した後で、出力カラースペースに変換します。 複数のレイヤーカラースペースが含まれる場合は、マージ前に各レイヤーが出力カラースペースに変換されます。

>[!NOTE]
>
>コマンド `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`、および `op_saturation=` は、RGB操作です。 これらの操作は、レイヤのカラースペースにRGBのピクセルタイプが含まれる場合にのみ、カラーの正確性を維持します。 RGB以外の場合、データは純粋な色変換を使用してRGBに変換され、結果の色の正確性は制限されます。 このようなレイヤのレイヤカラースペースは、不確定と見なす必要があります。

色変換オプションは、 `icc=` または、 `icc=` が指定されていない場合、は次の値を持ちます。 `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`、および `attribute::IccDither`.

## カラープロファイルの埋め込み {#section-261ebbae5ce046589a776ca972380052}

出力カラースペースの ICC カラープロファイル（使用可能な場合）は、 `iccEmbed=`.

## ICC プロファイルの管理 {#section-eb210e4b44e64e2c8b80ee59216c5555}

サーバが使用するすべてのカラープロファイルは、ICC の仕様に準拠している必要があります。 ICC プロファイルファイルには通常、 [!DNL .icc] または [!DNL .icm] ファイルサフィックスとは、画像データファイルと共に配置されます。

出力プロファイルは `icc=` コマンドを使用する場合は、デフォルトのカタログまたは画像カタログの ICC プロファイルマップにすべてのプロファイルファイルを登録し、ショートカット識別子 ( `icc::Name`) を使用します。

で参照されているすべての ICC プロファイル `catalog::IccProfile` および `attribute::IccProfile*` は、画像またはデフォルトカタログの ICC プロファイルマップに登録する必要があります。

## 制限事項 {#section-fb50ede40b124b89b30679da29782ab5}

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされます。

## 含まれる ICC カラープロファイル {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

画像サービングには、デフォルトのAdobeカタログにほとんどの標準の画像 ICC プロファイルが含まれます。 これらのプロファイルには、共通名 (Photoshopで表示されるように ) でアクセスすることも、識別子を少し短くしてアクセスすることもできます。 次の表に、すべての標準 ICC プロファイルを示します。 でプロファイルを参照する場合 `icc=` コマンドの共通名で、スペースは次のようにエンコードする必要があります。 `%20`.

追加のプロファイルを、デフォルトのカタログまたは特定の画像カタログのいずれかの標準プロファイルに追加できます。 詳しくは、 [ICC プロファイルマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) 」を参照してください。

>[!NOTE]
>
>次の表は、 *Dynamic Media Hybrid* のみ（実行中） `dynamicmedia` 実行モード )。

| 識別子 | 共通名 | ファイル名 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | ADOBE RGB(1998) | AdobeRGB1998.icc |
| `AppleRGB` | AppleRGB | AppleRGB.icc |
| `CIERGB` | CIERGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatchRGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhotoRGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb カラースペースプロファイル.icm |
| `WideGamutRGB` | 広域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 新聞 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | 米国新聞スプリント (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 のデフォルト CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 のデフォルト CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 非コート FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Web Coated SWOP 2006 Grade 3 用紙 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Web Coated SWOP 2006 Grade 5 用紙 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

次の表は、 *Dynamic Media Classic Image Serving* および *Dynamic Media* ( 実行中 `dynamicmedia_scene7` 実行モード )。

| 識別子 | 共通名 | ファイル名 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | ADOBE RGB(1998) | AdobeRGB1998.icc |
| `AppleRGB` | AppleRGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatchRGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhotoRGB | ProPhotoRGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb カラースペースプロファイル.icm |
| `WideGamutRGB` | 広域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 新聞 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 のデフォルト CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 のデフォルト CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 非コート FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | 米国新聞スプリント (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Web Coated SWOP 2006 Grade 3 用紙 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Web Coated SWOP 2006 Grade 5 用紙 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## 関連項目 {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC プロファイルマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
