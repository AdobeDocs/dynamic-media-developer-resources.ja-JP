---
title: 画像サービングカラーマネジメント
description: 画像サービングは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
TQID: 'https://experienceleague.adobe.com/IzOzGIHXhgknu9Wms73sua9vEF17EemCmaWPByRAp5M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1243
ht-degree: 0%

---

# 画像サービングカラーマネジメント{#image-serving-color-management}

画像サービングは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。

## デフォルトのカラースペース {#section-8cfe60808bce49968091995e4e521dba}

各画像カタログ（およびデフォルトカタログ）は、このカタログのデフォルトカラースペースを構成するICC プロファイルのセットを定義できます。1つの入力プロファイルと1つの出力プロファイルはそれぞれ、グレースケール、RGB、CMYK データに対して使用されます。 を参照
[属性：:IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[属性：:IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[属性：:IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[属性：:IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md)。

## 入力カラースペース {#section-9f08e2c1b6aa4fe4815be174972c1944}

Sourceの画像は、ICC プロファイルを埋め込んで、入力カラースペースを定義できます。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する該当する画像カタログの`attribute::IccProfileSrc*`が使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*`が使用されます。 カタログ属性が定義されていない場合、画像はカラーマネジメントされず、単純な変換のみが適用されます。

## 出力カラースペース {#section-b517bca622b64dcfa7defba6035d0716}

リクエストの最終画像結果のカラースペースは、`icc=` コマンドで定義されます。 `icc=`が指定されていない場合、出力画像のピクセルタイプに対応するデフォルトの出力カラースペース（リクエストのメインカタログから）が出力カラースペースとして使用されます。 メインカタログまたはデフォルトカタログで出力プロファイルが定義されておらず、ベースレイヤーが出力ピクセルタイプに一致する埋め込みプロファイルを持つ画像である場合、そのプロファイルが出力カラースペースに使用されます。 それ以外の場合、出力カラースペースは未定義のままになります。ピクセルタイプ間で変換する場合は、単純なカラー変換のみが適用され、出力画像にカラープロファイルを埋め込むことはできません。

ネストまたは埋め込まれた画像サービング要求の出力カラースペースは、外部の埋め込み要求の出力カラースペースと常に同じです。

## べた塗 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

`color=`、`bgcolor=`、またはRTF コマンド `\iscolortbl`で指定されたカラー値は、カラー値にサフィックス &#39;S&#39;が含まれている場合は入力カラースペースに関連付けられ、そうでない場合は出力カラースペースに関連付けられます。 `bgc=`またはRTF コマンド `\colortbl`と`\cmykcolortbl`で指定されたカラー値は、対応するデフォルトまたは実際の出力カラースペースに常に関連付けられます。

>[!NOTE]
>
>現時点では、`bgc=`はカラーマネジメントに完全に関与していません。`bgc=`で指定した場合、「S」のサフィックスは無視され、`bgc=`で指定したカラー値のピクセルタイプが出力画像のピクセルタイプと異なる場合はナイーブ変換が適用されます。 それ以外の場合、`bgc=`は実際の出力カラースペースに関連付けられます。

## ネストされたリクエストと埋め込まれたリクエスト {#section-bdda638c31504f26a77e51ebb1ea6e3b}

ネストされたIS リクエストと埋め込まれたIR リクエストの出力カラースペースは、ネストされたリクエストが`icc=`を持つ明示的な出力カラースペースを指定しない限り、最も外側のリクエストの出力カラースペースに自動的に設定されます。 さらに、ネストされた/埋め込まれたリクエストは、最外側のリクエストのメインカタログからデフォルトの出力カラースペースを継承して、単色の値を一貫して処理できるようにします。

## 色空間変換 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

画像サービングでは、通常、処理中にカラー変換を遅らせます。 画像のすべてのレイヤーのカラースペースが同じ場合、出力カラースペースへの変換は、結合と最終的な拡大・縮小の後に行われます。 複数のレイヤーカラースペースが含まれる場合、各レイヤーは結合の前に出力カラースペースに変換されます。

>[!NOTE]
>
>コマンド `op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`および`op_saturation=`はRGB操作です。 これらの操作は、レイヤーカラースペースにRGB ピクセルタイプがある場合にのみ、カラーの忠実度を維持します。 RGB以外の場合、データは単純なカラー変換を使用してRGBに変換され、結果のカラーの忠実度は制限されます。 そのようなレイヤーのレイヤーのカラースペースは不確定と見なされます。

色変換オプションは`icc=`で提供されますが、`icc=`が指定されていない場合は`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`、および`attribute::IccDither`で提供されます。

## カラープロファイルの埋め込み {#section-261ebbae5ce046589a776ca972380052}

出力カラースペースのICC カラープロファイルが使用可能な場合は、`iccEmbed=`を指定して応答画像に埋め込むことができます。

## ICC プロファイルの管理 {#section-eb210e4b44e64e2c8b80ee59216c5555}

サーバーが使用するすべてのカラープロファイルは、ICC仕様に準拠している必要があります。 ICC プロファイルファイルには通常、[!DNL .icc]または[!DNL .icm]個のファイル サフィックスが含まれており、画像データファイルと同じ場所に配置されます。

出力プロファイルは、`icc=` コマンドでファイルパスまたは名前で指定できますが、デフォルトカタログまたは画像カタログのICC プロファイルマップにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカット識別子（`icc::Name`）を使用することをお勧めします。

`catalog::IccProfile`および`attribute::IccProfile*`で参照されているすべてのICC プロファイルは、画像またはデフォルトカタログのICC プロファイルマップに登録する必要があります。

## 制限 {#section-fb50ede40b124b89b30679da29782ab5}

現時点では、CMYK、RGB、およびグレースケールのカラースペースのみがサポートされています。

## ICC カラープロファイルを含む {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

画像サービングには、デフォルトの画像カタログに標準のAdobe ICC プロファイルが含まれています。 これらのプロファイルには、共通の名前（例えば、Photoshopで見られる）またはIDが少し短い名前でアクセスできます。 次の表に、すべての標準ICC プロファイルを示します。 `icc=` コマンドで共通の名前でプロファイルを参照する場合、スペースは`%20`としてエンコードする必要があります。

標準プロファイルには、デフォルトカタログまたは特定の画像カタログのいずれかに追加プロファイルを追加できます。 詳しくは、[ICC プロファイルマップ リファレンス ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)を参照してください。

>[!NOTE]
>
>次の表は、*Dynamic Media Hybrid*&#x200B;にのみ適用されます（`dynamicmedia`実行モードで実行）。

| 識別子 | 共通の名前 | ファイル名 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC （1953） | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb カラースペース Profile.icm |
| `WideGamutRGB` | 広域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 （ISO 12647-2:2004） | CoatedFOGRA27.icc |
| `CoatedFogra39` | コーティングされたFOGRA39 （ISO 12647-2:2004） | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 （ISO 12647-2:2004） | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | ヨーロッパ ISO コーティングされたFOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | ユーロスケール Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | ジャパンカラー2002新聞 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated （Ad） | JapanWebCoated.icc |
| `NewsprintSNAP2007` | US Newsprint （SNAP 2007） | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 Default CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 Default CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 未処理のFOGRA29 （ISO 12647-2:2004） | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated （SWOP） v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web コーティングされたFOGRA28 （ISO 12647-2:2004） | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | ウェブコーティングされたSWOP 2006 グレード 3紙 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | ウェブコーティングされたSWOP 2006 グレード 5紙 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

次の表は、*Dynamic Media Classic Image Serving*&#x200B;および&#x200B;*Dynamic Media* （`dynamicmedia_scene7`実行モードで実行中）に適用されます。

| 識別子 | 共通の名前 | ファイル名 |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC （1953） | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb カラースペース Profile.icm |
| `WideGamutRGB` | 広域RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 （ISO 12647-2:2004） | CoatedFOGRA27.icc |
| `CoatedFogra39` | コーティングされたFOGRA39 （ISO 12647-2:2004） | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 （ISO 12647-2:2004） | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | ヨーロッパ ISO コーティングされたFOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | ユーロスケール塗装v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | ユーロスケール Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | ジャパンカラー2002新聞 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated （Ad） | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 Default CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 Default CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | 未処理のFOGRA29 （ISO 12647-2:2004） | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | US Newsprint （SNAP 2007） | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated （SWOP） v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web コーティングされたFOGRA28 （ISO 12647-2:2004） | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | ウェブコーティングされたSWOP 2006 グレード 3紙 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | ウェブコーティングされたSWOP 2006 グレード 5紙 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## 関連項目 {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter)、[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)、[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)、[属性：:IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;、[属性：:IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[属性：:IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)、[属性：:IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)、[ICC Profile Map](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)、[*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;[
