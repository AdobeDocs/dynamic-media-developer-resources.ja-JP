---
title: 画像サービングカラーマネジメント
description: 画像サービングは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペースコンバージョンをサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# 画像サービングカラーマネジメント{#image-serving-color-management}

画像サービングは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペースコンバージョンをサポートしています。

## デフォルトのカラースペース {#section-8cfe60808bce49968091995e4e521dba}

各画像カタログ（およびデフォルトカタログ）では、このカタログのデフォルトカラースペースを構成する ICC プロファイルのセット（グレースケール、RGB、CMYK のデータ用にそれぞれ 1 つの入力プロファイルと 1 つの出力プロファイル）を定義できます。 参照：
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md)。

## 入力カラースペース {#section-9f08e2c1b6aa4fe4815be174972c1944}

Source画像には、ICC プロファイルを埋め込んで、入力カラースペースを定義することもできます。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する適用可能な画像カタログのい `attribute::IccProfileSrc*` れかが使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*` が使用されます。 そのカタログ属性も定義されていない場合、画像は色管理されず、ネイティブな変換のみが適用されます。

## 出力カラースペース {#section-b517bca622b64dcfa7defba6035d0716}

リクエストの最終的な画像結果のカラースペースは、`icc=` コマンドで定義します。 `icc=` が指定されていない場合、出力画像のピクセルタイプに対応する（リクエストのメインカタログの）デフォルトの出力色空間が出力色空間として使用されます。 メインカタログまたはデフォルトカタログで出力プロファイルが定義されておらず、ベースレイヤーが出力ピクセルタイプと一致するプロファイルが埋め込まれた画像である場合、そのプロファイルが出力カラースペースに使用されます。 それ以外の場合、出力カラースペースは未定義のままになります。ピクセルタイプ間の変換時には単純なカラー変換のみが適用され、出力イメージにはカラープロファイルを埋め込むことはできません。

ネストされた埋め込み画像サービングリクエストの出力カラースペースは、外側の埋め込みリクエストの出力カラースペースと常に同じです。

## 単色 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

`color=`、`bgcolor=`、または RTF コマンド `\iscolortbl` で指定されたカラー値は、カラー値にサフィックス「S」が含まれている場合は入力カラースペースに関連付けられ、含まれていない場合は出力カラースペースに関連付けられます。 `bgc=` または RTF コマンド `\colortbl` および `\cmykcolortbl` で指定されたカラー値は、常に対応するデフォルトまたは実際の出力カラースペースに関連付けられます。

>[!NOTE]
>
>この際、`bgc=` はカラーマネジメントに完全には関与せず、`bgc=` で指定すると「S」サフィックスは無視され、`bgc=` で指定したカラー値のピクセルタイプが出力画像のピクセルタイプと異なる場合には、ナイーブ変換が適用される。 それ以外の場合は、`bgc=` れは実際の出力カラースペースに関連付けられます。

## ネストされたリクエストと埋め込まれたリクエスト {#section-bdda638c31504f26a77e51ebb1ea6e3b}

ネストされた IS 要求および埋め込まれた IR 要求の出力カラースペースは、ネストされた要求が `icc=` で明示的な出力カラースペースを指定しない限り、最も外側の要求の出力カラースペースに自動的に設定されます。 また、ネストされたリクエストや埋め込まれたリクエストは、最も外側のリクエストのメインカタログからデフォルトの出力カラースペースを継承し、ソリッドカラー値の一貫した処理を保証します。

## カラースペース変換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

画像サービングは通常、処理中にカラー変換を遅延させようとします。 画像のすべてのレイヤーのレイヤーカラースペースが同じ場合、出力カラースペースへの変換は、結合および最終スケーリングの後で行われます。 複数のレイヤーのカラースペースが含まれる場合、結合する前に、各レイヤーが出力カラースペースに変換されます。

>[!NOTE]
>
>`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=` および `op_saturation=` コマンドは、RGBの操作です。 これらの操作を行うと、レイヤーのカラースペースにRGB ピクセルタイプが含まれている場合にのみ、色の忠実性が維持されます。 RGB以外の場合は、ナイーブな色変換を使用してRGBに変換され、その結果、色の忠実性が制限されます。 このようなレイヤーのレイヤーカラースペースは、不定と見なす必要があります。

カラー変換オプションには、`icc=` が用意されています。`icc=` が指定されていない場合は、`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`、`attribute::IccDither` が用意されています。

## カラープロファイルの埋め込み {#section-261ebbae5ce046589a776ca972380052}

出力カラースペースの ICC カラープロファイルがある場合は、`iccEmbed=` を指定して応答画像に埋め込むことができます。

## ICC プロファイルの管理 {#section-eb210e4b44e64e2c8b80ee59216c5555}

サーバーで使用されるすべてのカラープロファイルは、ICC 仕様に準拠している必要があります。 ICC プロファイルファイルには通常、[!DNL .icc] または [!DNL .icm] のファイルサフィックスが付き、画像データファイルと一緒に配置されます。

出力プロファイルは `icc=` コマンドのファイル パス/名前で指定できますが、すべてのプロファイル ファイルを既定のカタログまたは画像カタログの ICC プロファイル マップに登録し、ファイル パスの代わりにショートカット識別子（`icc::Name`）を使用することをお勧めします。

`catalog::IccProfile` および `attribute::IccProfile*` で参照されるすべての ICC プロファイルは、画像またはデフォルトカタログの ICC プロファイルマップに登録される必要があります。

## 制限 {#section-fb50ede40b124b89b30679da29782ab5}

現時点では、CMYK、RGB、グレースケールカラースペースのみがサポートされています。

## 含まれる ICC カラープロファイル {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

画像サービングでは、デフォルトの画像カタログに、ほとんどの標準のAdobe ICC プロファイルが含まれています。 これらのプロファイルには、共通の名前（例えば、Photoshopに見られる）を使用するか、識別情報をわずかに短くすることでアクセスできます。 次の表に、すべての標準 ICC プロファイルを示します。 `icc=` コマンドでプロファイルを共通名で参照する場合は、スペースを `%20` としてエンコードする必要があります。

追加のプロファイルは、標準プロファイル（デフォルトカタログまたは特定の画像カタログ）に追加できます。 詳しくは、[ICC プロファイルマップ参照 ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) を参照してください。

>[!NOTE]
>
>次の表は、（実行モードで実行されている *Dynamic Media ハイブリッド* のみ `dynamicmedia` 適用されます。

| 識別子 | 共通名 | ファイル名 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | AppleRGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC （1953） | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb カラースペース プロファイル.icm |
| `WideGamutRGB` | 広色域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 （ISO 12647-2:2004） | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 （ISO 12647-2:2004） | CoatedFOGRA39.icc |
| `CoatedGraCol` | コート GRACoL 2006 （ISO 12647-2:2004） | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated （Ad） | JapanWebCoated.icc |
| `NewsprintSNAP2007` | 米国新聞記事（スナップ 2007） | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 デフォルト CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 デフォルト CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 （ISO 12647-2:2004） | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated （SWOP） v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 （ISO 12647-2:2004） | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Web Coated SWOP 2006 Grade 3 用紙 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Web Coated SWOP 2006 Grade 5 用紙 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

次の表は、*Dynamic Media Classic画像サービング* および *Dynamic Media* （実行モードで動作） `dynamicmedia_scene7` 適用されます。

| 識別子 | 共通名 | ファイル名 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | AppleRGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC （1953） | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb カラースペース プロファイル.icm |
| `WideGamutRGB` | 広色域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 （ISO 12647-2:2004） | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 （ISO 12647-2:2004） | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | コート GRACoL 2006 （ISO 12647-2:2004） | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated （Ad） | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 デフォルト CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 デフォルト CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 （ISO 12647-2:2004） | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | 米国新聞記事（スナップ 2007） | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated （SWOP） v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 （ISO 12647-2:2004） | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Web Coated SWOP 2006 Grade 3 用紙 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Web Coated SWOP 2006 Grade 5 用紙 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## 関連項目 {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter)、[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)、[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)、[attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;、[attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;、[attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)、[attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)、[ICC プロファイルマップ参照 ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)、[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) [&#128279;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、bgc=reference
