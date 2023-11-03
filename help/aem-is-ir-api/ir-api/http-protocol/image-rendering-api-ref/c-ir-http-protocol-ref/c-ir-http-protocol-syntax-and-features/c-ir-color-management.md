---
description: 画像レンダリングは、ICC(International Color Consortium) の仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。
solution: Experience Manager
title: 画像レンダリングのカラーマネジメント*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# 画像レンダリングのカラーマネジメント*{#image-rendering-color-management}

画像レンダリングは、ICC(International Color Consortium) の仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。

**制限事項**

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされます。

キャビネットスタイルファイル (.vnc) と窓カバリングスタイルファイル ( [!DNL .vnw]) は色管理されず、作業用カラースペースに存在すると見なされます。

**関連項目**

[International Color Consortium](https://www.color.org/index.xalter) , [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , ICC プロファイルマップ

## 初期設定のカラースペース {#section-8ce27edf42e746febe4654f8f19b9c0c}

各画像カタログ（およびデフォルトのカタログ）は、一連の ICC プロファイルを定義できます。 これらのプロファイルは、このカタログのデフォルトのカラースペースを構成します。各カラースペースは、グレースケール、RGB、CMYK データ ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`、および `attribute::IccProfileSrcCmyk`) をクリックします。

特定の画像または他のオブジェクトのデフォルトのカラースペースは、画像のピクセルタイプに基づいて、カタログのデフォルトプロファイルから選択されます。

## 入力カラースペース {#section-660f661a7e954df4b451e34134195276}

マテリアル画像は、ICC プロファイルを埋め込んで、入力カラースペースを定義できます。 ソース画像にプロファイルが埋め込まれていない場合、 `attribute::IccProfileSrc*` ソース画像のピクセルタイプに対応する適用可能な画像カタログのを使用する。 画像カタログでこの属性が定義されていない場合、 `attribute::IccProfile*` が使用されます。 そのカタログ属性も定義されていない場合、画像は色管理されず、単純な変換のみが適用されます。

## 作業用カラースペース {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常、作業用カラースペースは、ビネットに埋め込まれた ICC カラープロファイルによって定義されます。 ビネットにプロファイルが含まれていない場合、デフォルトのRGB入力プロファイル ( `attribute::IccProfileSrcRgb` （セッションカタログの）は、作業用カラースペースに使用されます。

すべてのレンダリング操作は、作業用カラースペースで実行されます。

**重要：** 作業用カラースペースの ICC プロファイルは、入力および出力変換をサポートする必要があります。 出力専用プロファイルを作業用カラースペースとして使用した場合、IR はマテリアルを変換できません。 同じ作業用カラースペースにマテリアルが存在する場合は、このようなカラープロファイルを引き続き使用できます。 他の色空間でマテリアルを適用しようとすると失敗する。

## 明示的なカラー値 {#section-31727bf1b23e477ca92572fbbf422d2f}

RGBの色の値 `color=`, `bgc=`, `catalog::BgColor`、および `catalog::Color` は、現在の作業用カラースペースに存在すると想定されます。

## 材料データファイル {#section-33f7a170a6664c02b8479fb89cc0aea3}

マテリアルイメージファイル（テクスチャイメージとデカールイメージ）は、RGB、グレースケール、CMYK のピクセルタイプを持つことができ、カラープロファイルを埋め込むことができます。 カラープロファイルが埋め込まれていない場合、初期設定の入力カラースペースが画像に関連付けられます（例えば、画像のピクセルタイプに対応するマテリアルカタログのカラープロファイル）。

ネストされた画像サービング要求または画像レンダリング要求から取得されたマテリアル画像には、通常、カラープロファイルが含まれます。 そうでない場合、画像は、ピクセルタイプに対応するデフォルトの入力カラースペースに関連付けられます。

画像ファイルのカラースペースが作業用カラースペースと異なる場合は、正確なカラー変換を使用して作業用カラースペースに変換します。 プロファイルが埋め込まれておらず、デフォルトの入力プロファイルが定義されていない場合は、ネイブタイプの変換が使用されます。

キャビネットスタイルファイル ( [!DNL .vnc]) またはウィンドウカバリングファイル ( [!DNL .vnw]) カラープロファイルを埋め込まず、常に作業用カラースペースと見なされます。

## 出力カラースペース {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

すべてのレンダリング操作は、作業用カラースペースで実行されます。 要求で `icc=` 」コマンドを使用すると、データはエンコードされる直前にそのカラースペースに変換され、クライアントに返されます。 カラーマネジメントが無効な場合、必要に応じて、グレースケールまたは CMYK への変換が正確に行われます。

## 埋め込みカラープロファイル {#section-5ff733832d38429fbe02b3c1e9bb94a9}

レンダリングされた画像に関連付けられたカラープロファイルを応答画像に埋め込むには、以下の指定を行います。 `iccEmbed=` リクエストに対して。

次の場合 `icc=` が指定されていない場合、作業用カラースペースの ICC プロファイルが埋め込まれます。 カラーマネジメントが無効で、でプロファイルが指定されていない場合、プロファイルは埋め込まれません。 `icc=`.

## ICC プロファイル［ICC ぷろふぁいる］ {#section-afeb76068b5042adb83261638e450140}

サーバが使用するすべてのカラープロファイルは、ICC の仕様に準拠している必要があります。 ICC プロファイルファイルには通常、 [!DNL .icc] または [!DNL .icm] ファイルサフィックスとは、マテリアルデータファイルと共に配置されます。

出力プロファイルは `icc=` コマンドを使用する場合は、デフォルトのカタログまたは特定のマテリアルカタログの ICC プロファイルマップにすべてのプロファイルファイルを登録し、ショートカット識別子 ( `icc::Name`) を使用します。

作業プロファイルは、マテリアルカタログまたはデフォルトカタログの ICC プロファイルマップに登録する必要があります。
