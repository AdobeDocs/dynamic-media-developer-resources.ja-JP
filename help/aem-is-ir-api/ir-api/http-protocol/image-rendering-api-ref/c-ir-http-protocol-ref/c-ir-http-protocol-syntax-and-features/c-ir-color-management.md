---
description: 画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。
seo-description: 画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。
seo-title: 画像レンダリングのカラーマネジメント*
solution: Experience Manager
title: 画像レンダリングのカラーマネジメント*
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# 画像レンダリングのカラーマネジメント*{#image-rendering-color-management}

画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。

**制限**

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされています。

キャビネットスタイルファイル(.vnc)とウィンドウカバリングスタイルファイル( [!DNL .vnw])は、色管理されず、作業用カラースペースに存在すると見なされます。

**関連項目**

[International Color Consortium](http://www.color.org/index.xalter) , [ , `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ , `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` Consortium `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , ICC `attribute::IccBlackPointCompensation``attribute::IccDither` Profile maps

## 初期設定のカラースペース {#section-8ce27edf42e746febe4654f8f19b9c0c}

各画像カタログ（および初期設定のカタログ）で、ICCプロファイルのセットを定義できます。 これらのプロファイルは、このカタログの初期設定のカラースペースを構成します。1つの入力と1つの出力プロファイルは、グレースケール、RGB、CMYKデータ(、、、、および、各デー `attribute::IccProfileRgb`タ)に対 `attribute::IccProfileGray`応し `attribute::IccProfileCmyk`てい `attribute::IccProfileSrcRgb``attribute::IccProfileSrcGray``attribute::IccProfileSrcCmyk`ます。

特定の画像または他のオブジェクトの初期設定のカラースペースは、画像のピクセルタイプに基づいて、カタログの初期設定のプロファイルから選択されます。

## 入力カラースペース {#section-660f661a7e954df4b451e34134195276}

マテリアル画像には、入力カラースペースを定義するICCプロファイルが埋め込まれる場合があります。 ソース画像にプロファイルが埋め込まれていない場合は、ソ `attribute::IccProfileSrc*` ース画像のピクセルタイプに対応する適用可能な画像カタログのプロファイルが使用されます。 この属性が画像カタログで定義されていない場合、が使 `attribute::IccProfile*` 用されます。 カタログ属性も定義されていない場合、画像はカラーマネジメントされず、単純な変換のみが適用されます。

## 作業用カラースペース {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常、作業用カラースペースは、ビネットに埋め込まれたICCカラープロファイルによって定義されます。 ビネットにプロファイルが含まれていない場合は、（セッションカタログの）初期 `attribute::IccProfileSrcRgb` 設定のRGB入力プロファイルが作業用カラースペースに使用されます。

すべてのレンダリング操作は、作業用カラースペースで実行されます。

**重要：** 作業用カラースペースのICCプロファイルは、入力変換と出力変換をサポートしている必要があります。 出力専用のプロファイルが作業用カラースペースとして使用されている場合、IRはマテリアルを変換できません。 同じ作業用カラースペースにマテリアルが存在する場合は、このようなカラープロファイルを使用できます。 他のカラースペースでマテリアルを適用しようとすると失敗します。

## 明示的なカラー値 {#section-31727bf1b23e477ca92572fbbf422d2f}

、、およびで指定され `color=`たRGBカ `bgc=`ラー値 `catalog::BgColor`は、現在 `catalog::Color` の作業カラースペースに存在すると見なされます。

## 材料データファイル {#section-33f7a170a6664c02b8479fb89cc0aea3}

マテリアルイメージファイル（テクスチャイメージとデカールイメージ）には、RGB、グレースケール、またはCMYKのピクセルタイプを含め、カラープロファイルを埋め込むことができます。 カラープロファイルが埋め込まれていない場合、初期設定の入力カラースペースは画像に関連付けられます（例えば、画像のピクセルタイプに対応するマテリアルカタログのカラープロファイル）。

ネストされた画像サービングまたは画像レンダリングの要求から取得されたマテリアル画像には、通常、カラープロファイルが含まれます。 そうでない場合、画像は、ピクセルの種類に対応する初期設定の入力カラースペースに関連付けられます。

画像ファイルのカラースペースが作業用カラースペースと異なる場合、正確なカラー変換を使用して作業用カラースペースに変換します。 プロファイルが埋め込まれておらず、デフォルトの入力プロファイルが定義されていない場合は、Nayve型の変換が使用されます。

キャビネットスタイルのファイル( [!DNL .vnc])や窓カバリングのファイル( [!DNL .vnw])など、他のマテリアルデータファイルは、カラープロファイルを埋め込まず、常に作業用カラースペースにあると見なされます。

## 出力カラースペース {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

すべてのレンダリング操作は、作業用カラースペースで行われます。 要求でコマンドで別のカラープロファイルが指定されている場合、データはエンコードされる直前にそのカラースペースに変換され、クライアントに返されます。 `icc=` カラーマネジメントが無効な場合、必要に応じて純粋な変換が使用され、グレースケールまたはCMYKに変換されます。

## 埋め込みカラープロファイル {#section-5ff733832d38429fbe02b3c1e9bb94a9}

要求に対して指定することで、レンダリングされた画像に関連付けられたカラープロファイルを応答画像 `iccEmbed=` に埋め込むことができます。

を指定 `icc=` しない場合、作業用カラースペースのICCプロファイルが埋め込まれます。 カラーマネジメントが無効で、でプロファイルが指定されていない場合、プロファイルは埋め込まれませ `icc=`ん。

## ICC プロファイル［ICC ぷろふぁいる］ {#section-afeb76068b5042adb83261638e450140}

サーバが使用するすべてのカラープロファイルは、ICC仕様に準拠している必要があります。 ICCプロファイルファイルは、通常、ファ [!DNL .icc] イルサ [!DNL .icm] フィックスまたはファイルサフィックスを持ち、マテリアルデータファイルと共に配置されます。

出力プロファイルはコマンドでファイルパス/名前で指定できますが、初期設定のカタログまたは特定のマテリアルカタログのICCプロファイルマップにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカット識別子( `icc=``icc::Name`)を使用することをお勧めします。

作業プロファイルは、マテリアルカタログまたは初期設定のカタログのICCプロファイルマップに登録する必要があります。
