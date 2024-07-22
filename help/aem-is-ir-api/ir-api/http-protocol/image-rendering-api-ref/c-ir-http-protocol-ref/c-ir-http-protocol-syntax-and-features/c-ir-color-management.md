---
description: 画像レンダリングでは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。
solution: Experience Manager
title: 画像レンダリングのカラーマネジメント *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# 画像レンダリングのカラーマネジメント *{#image-rendering-color-management}

画像レンダリングでは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。

**制限**

現時点では、CMYK、RGB、グレースケールカラースペースのみがサポートされています。

キャビネット スタイル ファイル（.vnc）および窓隠しスタイル ファイル（[!DNL .vnw]）は色管理されておらず、作業カラースペースに存在すると見なされます。

**関連トピック**

[International Color Consortium](https://www.color.org/index.xalter)、[`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)、[`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)、`attribute::IccProfile*`、`attribute::IccProfileSrc*`、`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`、`attribute::IccDither`、ICC プロファイルマップ

## デフォルトのカラースペース {#section-8ce27edf42e746febe4654f8f19b9c0c}

各画像カタログ（およびデフォルトのカタログ）で、一連の ICC プロファイルを定義できます。 これらのプロファイルは、このカタログのデフォルトのカラースペースを構成します。グレースケール、RGB、CMYK データ（`attribute::IccProfileRgb`、`attribute::IccProfileGray`、`attribute::IccProfileCmyk`、`attribute::IccProfileSrcRgb`、`attribute::IccProfileSrcGray` および `attribute::IccProfileSrcCmyk`）ごとに 1 つの入力プロファイルと 1 つの出力プロファイルです。

特定の画像またはその他のオブジェクトのデフォルトのカラースペースは、画像のピクセルタイプに基づいて、カタログのデフォルトプロファイルから選択されます。

## 入力カラースペース {#section-660f661a7e954df4b451e34134195276}

マテリアル画像は、入力カラースペースを定義するために ICC プロファイルを埋め込むことがあります。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する適用可能な画像カタログのい `attribute::IccProfileSrc*` れかが使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*` が使用されます。 そのカタログ属性も定義されていない場合、画像は色管理されず、ネイティブな変換のみが適用されます。

## 作業カラースペース {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常、作業カラースペースは、ビネットに埋め込まれた ICC カラープロファイルによって定義されます。 ビネットにプロファイルが含まれていない場合、デフォルトのRGB入力プロファイル（セッションカタログの `attribute::IccProfileSrcRgb`）が作業用カラースペースに使用されます。

すべてのレンダリング操作は、作業カラースペースで実行されます。

**重要：** 作業カラースペースの ICC プロファイルは、入力および出力変換をサポートする必要があります。 出力専用プロファイルが作業カラースペースとして使用されている場合、IR はマテリアルを変換できません。 このようなカラープロファイルは、同じ作業カラースペースにマテリアルが存在する場合でも使用できます。 他のカラースペースにマテリアルを適用しようとすると失敗します。

## 明示的なカラー値 {#section-31727bf1b23e477ca92572fbbf422d2f}

`color=`、`bgc=`、`catalog::BgColor`、`catalog::Color` で指定されたRGBカラー値は、現在の作業カラースペースに存在すると見なされます。

## マテリアル データ ファイル {#section-33f7a170a6664c02b8479fb89cc0aea3}

マテリアル イメージ ファイル（テクスチャ イメージとデカル イメージ）には、RGB、グレースケール、または CMYK ピクセル タイプを使用でき、カラープロファイルを埋め込むことができます。 カラープロファイルが埋め込まれていない場合、デフォルトの入力カラースペースは画像に関連付けられます（例えば、画像のピクセルタイプに対応する材料カタログのカラープロファイルなど）。

ネストされた画像サービングまたは画像レンダリングのリクエストから取得されたマテリアル画像には、通常、カラープロファイルが含まれています。 そうでない場合、画像はピクセルタイプに対応するデフォルトの入力カラースペースに関連付けられます。

画像ファイルのカラースペースが作業カラースペースと異なる場合は、正確な色変換を使用して作業カラースペースに変換します。 ネイティブ型変換は、プロファイルが埋め込まれておらず、デフォルトの入力プロファイルが定義されていない場合に使用されます。

キャビネット スタイル ファイル（[!DNL .vnc]）や窓覆いファイル（[!DNL .vnw]）などの他のマテリアル データ ファイルは、カラープロファイルを埋め込まず、常に作業カラースペースにあると見なされます。

## 出力カラースペース {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

すべてのレンダリング操作は、作業カラースペースで行われます。 リクエストで `icc=` コマンドを使用して別のカラープロファイルを指定すると、データはエンコードされる直前にそのカラースペースに変換され、クライアントに返されます。 カラーマネジメントが無効の場合、グレースケールまたは CMYK に変換するために必要であれば、ネイティブ変換が使用されます。

## 埋め込みカラープロファイル {#section-5ff733832d38429fbe02b3c1e9bb94a9}

リクエストの `iccEmbed=` を指定することで、レンダリングされた画像に関連付けられたカラープロファイルを応答画像に埋め込むことができます。

`icc=` が指定されていない場合、作業カラースペースの ICC プロファイルが埋め込まれます。 カラーマネジメントが無効になっていて、`icc=` でプロファイルが指定されていない場合、プロファイルは埋め込まれません。

## ICC プロファイル［ICC ぷろふぁいる］ {#section-afeb76068b5042adb83261638e450140}

サーバーで使用されるすべてのカラープロファイルは、ICC 仕様に準拠している必要があります。 ICC プロファイル ファイルには通常、[!DNL .icc] または [!DNL .icm] のファイル拡張子が付き、マテリアル データ ファイルと一緒に配置されます。

出力プロファイルは `icc=` コマンドのファイル パス/名前で指定できますが、すべてのプロファイル ファイルを既定のカタログまたは特定の材料カタログの ICC プロファイル マップに登録し、ファイル パスの代わりにショートカット識別子（`icc::Name`）を使用することをお勧めします。

作業プロファイルは、材料カタログまたはデフォルトカタログの ICC プロファイルマップに登録する必要があります。
