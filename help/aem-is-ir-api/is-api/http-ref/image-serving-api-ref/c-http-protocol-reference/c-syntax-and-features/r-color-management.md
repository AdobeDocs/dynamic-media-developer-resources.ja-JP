---
description: 画像サービングでは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換がサポートされています。
seo-description: 画像サービングでは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換がサポートされています。
seo-title: 画像サービングのカラーマネジメント
solution: Experience Manager
title: 画像サービングのカラーマネジメント
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 0%

---


# 画像サービングのカラーマネジメント{#image-serving-color-management}

画像サービングでは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換がサポートされています。

## デフォルトのカラースペース{#section-8cfe60808bce49968091995e4e521dba}

各画像カタログ（および初期設定のカタログ）では、このカタログの初期設定のカラースペースを構成する一連のICCプロファイルを定義できます。各カタログは、グレースケール、RGB、CMYKデータ用に1つの入力画像と1つの出力プロファイルです。 ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`、` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`、` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`、` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`、` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`、` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`を参照してください。

## 入力カラースペース{#section-9f08e2c1b6aa4fe4815be174972c1944}

ソース画像は、ICCプロファイルを埋め込んで入力カラースペースを定義する場合があります。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する該当する画像カタログの`attribute::IccProfileSrc*`が使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*`が使用されます。 カタログ属性も定義されていない場合、画像はカラーマネージされず、単純な変換のみが適用されます。

## 出力カラースペース{#section-b517bca622b64dcfa7defba6035d0716}

リクエストの最終的なイメージ結果のカラースペースは、`icc=`コマンドで定義します。 `icc=`を指定しない場合、（要求のメインカタログからの）出力画像のピクセルタイプに対応する初期設定の出力カラースペースが出力カラースペースとして使用されます。 メインまたは初期設定のカタログに出力プロファイルが定義されていない場合に、ベースレイヤーが、出力ピクセルタイプに一致する埋め込みプロファイルを持つ画像の場合は、そのプロファイルが出力カラースペースに使用されます。 それ以外の場合、出力カラースペースは未定義のままです。ピクセルタイプ間の変換時には純粋なカラー変換のみが適用され、出力プロファイルにカラー画像は埋め込まれません。

入れ子/埋め込みの画像サービング要求の出力カラースペースは、常に、外側の埋め込み要求の出力カラースペースと同じです。

## べた塗り{#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

`color=`、`bgcolor=`、またはRTFコマンド`\iscolortbl`で指定されたカラー値は、カラー値にサフィックス「S」が含まれる場合は入力カラースペースに関連付けられ、それ以外の場合は出力カラースペースに関連付けられます。 `bgc=`またはRTFコマンド`\colortbl`と`\cmykcolortbl`で指定したカラー値は、常に、対応するデフォルトまたは実際の出力カラースペースに関連付けられます。

>[!NOTE]
>
>現時点で、`bgc=`はカラーマネジメントに完全には関与しません。`bgc=`で指定した場合は「S」サフィックスは無視され、`bgc=`で指定したカラー値のピクセルタイプが出力画像のピクセルタイプと異なる場合は純粋な変換が適用されます。 それ以外の場合は、`bgc=`は実際の出力カラースペースに関連付けられます。

## ネストされた、埋め込まれたリクエスト{#section-bdda638c31504f26a77e51ebb1ea6e3b}

入れ子にされたIS要求と埋め込まれたIR要求の出力カラースペースは、入れ子にされた要求で`icc=`を使用して明示的な出力カラースペースが指定されていない限り、自動的に最も外側の要求の出力カラースペースに設定されます。 また、ネスト/埋め込みのリクエストも、最も外側のリクエストのメインカタログからデフォルトの出力カラースペースを継承するので、べた塗りの値の処理が一貫して行われます。

## 色空間変換{#section-ca87b80b8e364ea59d8a92d87121b0fb}

画像サービングでは、通常、処理中に色の変換を遅らせようとします。 画像のすべてのレイヤーのカラースペースが同じである場合、出力カラースペースへの変換は、結合と最終的な拡大・縮小の後に行われます。 複数のレイヤーカラースペースが含まれる場合、各レイヤーは結合前に出力カラースペースに変換されます。

>[!NOTE]
>
>`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`、`op_saturation=`の各コマンドは、RGB演算です。 これらの操作は、レイヤーカラースペースにRGBピクセルタイプがある場合にのみ、カラーの忠実度を維持します。 RGB以外の場合、データは純粋なカラー変換を使用してRGBに変換され、結果の色の忠実度は限られます。 このようなレイヤーのレイヤーカラースペースは、不確定と見なす必要があります。

色変換オプションは、`icc=`、または`icc=`が指定されていない場合は`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`、`attribute::IccDither`で提供されます。

## 色プロファイルの埋め込み{#section-261ebbae5ce046589a776ca972380052}

出力カラースペースのICCカラープロファイルがある場合は、`iccEmbed=`を指定して、応答画像に埋め込むことができます。

## ICCプロファイルの管理{#section-eb210e4b44e64e2c8b80ee59216c5555}

サーバが使用するカラープロファイルはすべて、ICC仕様に準拠している必要があります。 ICCプロファイルファイルには通常、[!DNL .icc]または[!DNL .icm]のファイルサフィックスが付き、画像データファイルと共に配置されます。

出力プロファイルは`icc=`コマンドのファイルパス/名前で指定できますが、初期設定のカタログまたは画像カタログのICCプロファイルマップにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカット識別子(`icc::Name`)を使用することをお勧めします。

`catalog::IccProfile`と`attribute::IccProfile*`で参照されているすべてのICCプロファイルは、画像または初期設定のカタログのICCプロファイルマップに登録する必要があります。

## 制限{#section-fb50ede40b124b89b30679da29782ab5}

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされています。

## 含まれているICCカラープロファイル{#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

画像サービングでは、初期設定の画像カタログに、ほとんどの標準AdobeのICCプロファイルが含まれています。 これらのプロファイルは、共通名(Photoshopで見られるような名前)か、ある程度短い識別子を使用してアクセスできます。 次の表に、すべての標準ICCプロファイルをリストします。 `icc=`コマンド内のプロファイルを共通名で参照する場合は、スペースを`%20`としてエンコードする必要があります。

追加のプロファイルを標準プロファイル（初期設定のカタログまたは特定の画像カタログ）に追加できます。 詳しくは、[ICCプロファイルマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)を参照してください。

>[!NOTE]
>
>次の表は、*Dynamic Mediaハイブリッド*&#x200B;のみに適用されます（`dynamicmedia`実行モードで実行）。

|識別子|共通名|ファイル名|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgbカラースペースプロファイル.icm|
|`WideGamutRGB`|広域RGB|WideGamotRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspar|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop4の初期設定のCMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop5の初期設定のCMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|U.S. Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|米国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`WebCoated`|米国Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Web Coated SWOP 2006 Grade 3用紙|WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Web Coated SWOP 2006 Grade 5用紙|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|米国Web Uncoated v2|USWebUncoated.icc|

次の表は、*Dynamic Mediaクラシック(Scene7)画像サービング*&#x200B;と&#x200B;*Dynamic Media*（`dynamicmedia_scene7`実行モードで実行）に適用されます。

|識別子|共通名|ファイル名|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgbカラースペースプロファイル.icm|
|`WideGamutRGB`|広域RGB|WideGamotRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspar|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`PS4Default`|Photoshop4の初期設定のCMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop5の初期設定のCMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|米国Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|米国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|米国Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006 Grade 5用紙|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|米国Web Uncoated v2|USWebUncoated.icc|

## 関連項目 {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*,[attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),[attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [ICCプロファイルマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
