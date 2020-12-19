---
description: 画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。
seo-description: 画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。
seo-title: 画像レンダリングのカラーマネジメント*
solution: Experience Manager
title: 画像レンダリングのカラーマネジメント*
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---


# イメージレンダリングのカラーマネジメント*{#image-rendering-color-management}

画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。

**制限事項**

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされています。

キャビネットスタイルファイル(.vnc)および窓カバリングスタイルファイル([!DNL .vnw])は色管理されず、作業用カラースペースに存在すると見なされます。

**関連項目**

[International Color Consortium](http://www.color.org/index.xalter) , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,,, [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` ,,,,,,,,,,,,,,,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent`  `attribute::IccBlackPointCompensation`  `attribute::IccDither` , ICCプロファイルマップ

## デフォルトのカラースペース{#section-8ce27edf42e746febe4654f8f19b9c0c}

各画像カタログ（および初期設定のカタログ）は、一連のICCプロファイルを定義できます。 これらのプロファイルは、このカタログの初期設定のカラースペースを構成します。グレースケール、RGB、CMYKデータ(`attribute::IccProfileRgb`、`attribute::IccProfileGray`、`attribute::IccProfileCmyk`、`attribute::IccProfileSrcRgb`、`attribute::IccProfileSrcGray`、`attribute::IccProfileSrcCmyk`)用に1つの入力と1つの出力プロファイルです。

特定の画像または他のオブジェクトの初期設定のカラースペースは、画像のピクセルタイプに基づいて、カタログの初期設定のプロファイルから選択されます。

## 入力カラースペース{#section-660f661a7e954df4b451e34134195276}

マテリアル画像は、ICCプロファイルを埋め込んで入力カラースペースを定義する場合があります。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する該当する画像カタログの`attribute::IccProfileSrc*`が使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*`が使用されます。 カタログ属性も定義されていない場合、画像はカラーマネージされず、単純な変換のみが適用されます。

## 作業用カラースペース{#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常、作業用カラースペースは、ビネットに埋め込まれたICCカラープロファイルによって定義されます。 ビネットにプロファイルが含まれていない場合は、作業用カラースペースに、初期設定のRGB入力プロファイル（セッションカタログの`attribute::IccProfileSrcRgb`）が使用されます。

すべてのレンダリング操作は、作業用カラースペースで実行されます。

**重要：作業用カラースペ** ースのICCプロファイルは、入力変換と出力変換をサポートしている必要があります。出力のみのプロファイルを作業用カラースペースIRとして使用すると、マテリアルを変換できなくなります。 このようなカラープロファイルは、同じ作業用カラースペースにマテリアルが存在する場合にも使用できます。 他のカラースペースでマテリアルを適用しようとすると失敗します。

## 明示的なカラー値{#section-31727bf1b23e477ca92572fbbf422d2f}

`color=`、`bgc=`、`catalog::BgColor`および`catalog::Color`で指定されたRGBカラー値は、現在の作業カラースペースに存在すると見なされます。

## 材料データファイル{#section-33f7a170a6664c02b8479fb89cc0aea3}

マテリアルイメージファイル（テクスチャイメージとデカールイメージ）には、RGB、グレースケール、またはCMYKのピクセルタイプを含めることができ、カラープロファイルを埋め込むことができます。 カラープロファイルが埋め込まれていない場合、初期設定の入力カラースペースは画像に関連付けられます(例えば、画像のピクセルタイプに対応するマテリアルカタログのカラープロファイル)。

ネストされた画像サービングまたは画像レンダリング要求から取得されたマテリアル画像には、通常、カラープロファイルが含まれます。 そうでない場合、画像は、ピクセルタイプに対応する初期設定の入力カラースペースに関連付けられます。

画像ファイルのカラースペースが作業用カラースペースと異なる場合は、正確なカラー変換を使用して作業用カラースペースに変換します。 プロファイルが埋め込まれておらず、デフォルトの入力プロファイルが定義されていない場合は、Naive型の変換が使用されます。

キャビネットスタイルファイル([!DNL .vnc])や窓カバリングファイル([!DNL .vnw])など、他のマテリアルデータファイルは、カラープロファイルを埋め込まず、常に作業用カラースペースにあると見なされます。

## 出力カラースペース{#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

すべてのレンダリング操作は、作業用カラースペースで行われます。 要求で`icc=`コマンドで別の色プロファイルを指定した場合、データは、エンコードされる直前にその色空間に変換され、クライアントに返されます。 カラーマネジメントが無効な場合、必要に応じてグレースケールまたはCMYKに変換するためにネイティブ変換が使用されます。

## 埋め込みカラープロファイル{#section-5ff733832d38429fbe02b3c1e9bb94a9}

レンダリングされた画像に関連付けられたカラープロファイルは、要求に対して`iccEmbed=`を指定することで、応答画像に埋め込むことができます。

`icc=`を指定しない場合、作業用カラースペースのICCプロファイルが埋め込まれます。 カラーマネジメントが無効で、`icc=`でプロファイルが指定されていない場合、プロファイルは埋め込まれません。

## ICC プロファイル［ICC ぷろふぁいる］ {#section-afeb76068b5042adb83261638e450140}

サーバが使用するカラープロファイルはすべて、ICC仕様に準拠している必要があります。 ICCプロファイルファイルには通常、[!DNL .icc]または[!DNL .icm]のファイルサフィックスが付き、マテリアルデータファイルと共に配置されます。

出力プロファイルは`icc=`コマンドのファイルパス/名前で指定できますが、初期設定のカタログまたは特定のマテリアルカタログのICCプロファイルマップにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカットID(`icc::Name`)を使用することをお勧めします。

作業プロファイルは、マテリアルカタログまたは初期設定のカタログのICCプロファイルマップに登録する必要があります。
