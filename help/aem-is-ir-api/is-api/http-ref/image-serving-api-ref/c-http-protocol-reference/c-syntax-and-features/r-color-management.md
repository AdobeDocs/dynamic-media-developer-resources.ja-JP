---
description: 画像サービングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。
solution: Experience Manager
title: 画像サービングのカラーマネジメント
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# 画像サービングのカラーマネジメント{#image-serving-color-management}

画像サービングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。

## 初期設定のカラースペース {#section-8cfe60808bce49968091995e4e521dba}

各画像カタログ（およびデフォルトカタログ）は、このカタログのデフォルトカラースペースを構成するICCプロファイルのセットを定義できます。グレースケール、RGB、CMYKデータ用にそれぞれ1つの入力および1つの出力プロファイルです。 ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`、` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`、` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`、` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`、` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`、` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`を参照してください。

## 入力カラースペース {#section-9f08e2c1b6aa4fe4815be174972c1944}

ソース画像は、ICCプロファイルを埋め込んで入力カラースペースを定義する場合があります。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する該当する画像カタログの`attribute::IccProfileSrc*`が使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*`が使用されます。 そのカタログ属性も定義されていない場合、画像は色管理されず、単純な変換のみが適用されます。

## 出力カラースペース {#section-b517bca622b64dcfa7defba6035d0716}

要求の最終的なイメージ結果のカラースペースは、`icc=`コマンドで定義されます。 `icc=`を指定しない場合、出力画像のピクセルタイプに対応する（リクエストのメインカタログからの）デフォルトの出力カラースペースが出力カラースペースとして使用されます。 メインまたはデフォルトのカタログに出力プロファイルが定義されていない場合、出力ピクセルタイプに一致する埋め込みプロファイルを持つ画像がベースレイヤーに含まれている場合は、そのプロファイルが出力カラースペースに使用されます。 そうしないと、出力カラースペースが未定義のままになり、ピクセルタイプ間の変換時には純粋なカラー変換のみが適用され、出力画像にカラープロファイルを埋め込むことができません。

ネスト/埋め込み画像サービング要求の出力カラースペースは、常に、外部の埋め込み要求の出力カラースペースと同じです。

## べた塗り {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

`color=`、`bgcolor=`、またはRTFコマンド`\iscolortbl`で指定されたカラー値は、カラー値にサフィックス「S」が含まれる場合は入力カラースペースに関連付けられ、それ以外の場合は出力カラースペースに関連付けられます。 `bgc=`またはRTFコマンド`\colortbl`と`\cmykcolortbl`で指定されたカラー値は、常に、対応するデフォルトまたは実際の出力カラースペースに関連付けられます。

>[!NOTE]
>
>このとき、`bgc=`はカラーマネジメントに完全に関与しない — `bgc=`で指定された場合、「S」サフィックスは無視され、`bgc=`で指定されたカラー値のピクセルタイプが出力画像のピクセルタイプと異なる場合、純粋な変換が適用される。 それ以外の場合は、 `bgc=`は実際の出力カラースペースに関連付けられます。

## ネストされたリクエストと埋め込まれたリクエスト {#section-bdda638c31504f26a77e51ebb1ea6e3b}

ネストされたIS要求と埋め込みIR要求の出力カラースペースは、ネストされた要求で`icc=`を使用して明示的な出力カラースペースが指定されていない限り、最も外側の要求の出力カラースペースに自動的に設定されます。 さらに、ネスト/埋め込みリクエストも、最も外側のリクエストのメインカタログからデフォルトの出力カラースペースを継承し、べた塗りの値を一貫して処理します。

## カラースペースの変換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

通常、画像サービングは、処理中に色変換の遅延を試みます。 画像のすべてのレイヤーのカラースペースが同じ場合、マージおよび最終的な拡大・縮小の後で、出力カラースペースへの変換が行われます。 複数のレイヤーカラースペースが含まれる場合、各レイヤーはマージ前に出力カラースペースに変換されます。

>[!NOTE]
>
>コマンド`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`、`op_saturation=`はRGB操作です。 これらの操作は、レイヤーカラースペースにRGBピクセルタイプが含まれる場合にのみ、カラーの忠実性を維持します。 RGB以外の場合、データは純粋な色変換を使用してRGBに変換され、結果の色の忠実度は制限されます。 このようなレイヤのレイヤカラースペースは、不定と見なす必要があります。

色変換オプションは、 `icc=`または`icc=`が指定されていない場合は`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`、`attribute::IccDither`で指定します。

## カラープロファイルの埋め込み {#section-261ebbae5ce046589a776ca972380052}

出力カラースペースのICCカラープロファイル（ある場合）は、`iccEmbed=`を指定して応答画像に埋め込むことができます。

## ICCプロファイルの管理 {#section-eb210e4b44e64e2c8b80ee59216c5555}

サーバーで使用されるすべてのカラープロファイルは、ICC仕様に準拠している必要があります。 ICCプロファイルファイルは通常、[!DNL .icc]または[!DNL .icm]のファイルサフィックスを持ち、画像データファイルと共に配置されます。

出力プロファイルは`icc=`コマンドでファイルパス/名前で指定できますが、デフォルトのカタログまたは画像カタログのICCプロファイルマップにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカット識別子(`icc::Name`)を使用することをお勧めします。

`catalog::IccProfile`と`attribute::IccProfile*`で参照されるすべてのICCプロファイルは、画像またはデフォルトカタログのICCプロファイルマップに登録する必要があります。

## 制限事項 {#section-fb50ede40b124b89b30679da29782ab5}

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされています。

## 付属のICCカラープロファイル {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

画像サービングには、デフォルトのAdobeカタログのほとんどの標準の画像ICCプロファイルが含まれます。 これらのプロファイルは、共通名(Photoshopで確認できるように)または短い識別子を使用してアクセスできます。 次の表に、すべての標準ICCプロファイルを示します。 `icc=`コマンドでプロファイルを共通名で参照する場合は、スペースを`%20`としてエンコードする必要があります。

追加のプロファイルは、デフォルトのカタログまたは特定の画像カタログのいずれかの標準プロファイルに追加できます。 詳しくは、[ICCプロファイルマップのリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)を参照してください。

>[!NOTE]
>
>次の表は、*Dynamic Mediaハイブリッド*&#x200B;のみ（`dynamicmedia`実行モードで実行）に適用されます。

|識別子|共通名|ファイル名|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgbカラースペースProfile.icm|
|`WideGamutRGB`|広色域RGB|WideGamutRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|米国ニュースプリント(SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|米国Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|米国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|非コートFOGRA29 (ISO 12647-2:2004)|非コートFOGRA29.icc|
|`WebCoated`|米国Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Web Coated SWOP 2006 Grade 3用紙|WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Web Coated SWOP 2006 Grade 5用紙|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|米国Web Uncoated v2|USWebUncoated.icc|

次の表は、*Dynamic Media Classic画像サービング*&#x200B;および&#x200B;*Dynamic Media*（`dynamicmedia_scene7`実行モードで実行）に適用されます。

|識別子|共通名|ファイル名|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgbカラースペースProfile.icm|
|`WideGamutRGB`|広色域RGB|WideGamutRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|米国Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|米国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|非コートFOGRA29 (ISO 12647-2:2004)|非コートFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|米国ニュースプリント(SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|米国Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 Grade 3用紙|WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006 Grade 5用紙|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|米国Web Uncoated v2|USWebUncoated.icc|

## 関連項目 {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter)、 [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)、 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)、 [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*、 [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*、 [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、 [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)、 [属性：IcIcIcIcIcI](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
