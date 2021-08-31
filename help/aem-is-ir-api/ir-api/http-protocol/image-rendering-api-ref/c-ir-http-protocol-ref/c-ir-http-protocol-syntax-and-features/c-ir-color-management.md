---
description: 画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。
solution: Experience Manager
title: 画像レンダリングのカラーマネジメント*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# 画像レンダリングのカラーマネジメント*{#image-rendering-color-management}

画像レンダリングは、ICC(International Color Consortium)仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートします。

**制限事項**

現時点では、CMYK、RGB、グレースケールのカラースペースのみがサポートされています。

キャビネットスタイルファイル(.vnc)と窓カバースタイルファイル([!DNL .vnw])は色管理されず、作業用カラースペースに存在すると想定されます。

**関連項目**

[International Color Consortium](https://www.color.org/index.xalter) 、 [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) 、 [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) 、 `attribute::IccProfile*` 、 `attribute::IccProfileSrc*`、 `attribute::IccRenderIntent` 、 `attribute::IccBlackPointCompensation` 、 `attribute::IccDither` 、ICCプロファイルマップ

## 初期設定のカラースペース {#section-8ce27edf42e746febe4654f8f19b9c0c}

各画像カタログ（およびデフォルトのカタログ）は、ICCプロファイルのセットを定義できます。 これらのプロファイルは、このカタログのデフォルトカラースペースを構成します。グレースケール、RGBおよびCMYKデータ（ `attribute::IccProfileRgb`、 `attribute::IccProfileGray`、 `attribute::IccProfileCmyk`、 `attribute::IccProfileSrcRgb`、 `attribute::IccProfileSrcGray`および`attribute::IccProfileSrcCmyk` ）用に、それぞれ1つの入力および1つの出力プロファイルです。

特定の画像または他のオブジェクトのデフォルトカラースペースは、画像のピクセルタイプに基づいて、カタログのデフォルトプロファイルから選択されます。

## 入力カラースペース {#section-660f661a7e954df4b451e34134195276}

マテリアルイメージは、ICCプロファイルを埋め込んで入力カラースペースを定義する場合があります。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する該当する画像カタログの`attribute::IccProfileSrc*`が使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*`が使用されます。 そのカタログ属性も定義されていない場合、画像は色管理されず、単純な変換のみが適用されます。

## 作業用カラースペース {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常、作業用カラースペースは、ビネットに埋め込まれたICCカラープロファイルによって定義されます。 ビネットにプロファイルが含まれていない場合は、初期設定のRGB入力プロファイル（セッションカタログの`attribute::IccProfileSrcRgb`）が作業用カラースペースに使用されます。

すべてのレンダリング操作は、作業用カラースペースで実行されます。

**重要：** 作業用カラースペースのICCプロファイルは、入力変換と出力変換をサポートしている必要があります。出力専用プロファイルを作業用カラースペースとして使用すると、IRはマテリアルを変換できません。 同じ作業用カラースペースにマテリアルが存在する場合は、このようなカラープロファイルを引き続き使用できます。 他の色空間にマテリアルを適用しようとすると失敗します。

## 明示的なカラー値 {#section-31727bf1b23e477ca92572fbbf422d2f}

`color=`、`bgc=`、`catalog::BgColor`、`catalog::Color`で指定されたRGBカラー値は、現在の作業用カラースペースに存在すると見なされます。

## 材料データファイル {#section-33f7a170a6664c02b8479fb89cc0aea3}

マテリアルイメージファイル（テクスチャイメージとデカールイメージ）には、RGB、グレースケール、またはCMYKピクセルタイプを含め、カラープロファイルを埋め込むことができます。 カラープロファイルが埋め込まれていない場合、デフォルトの入力カラースペースが画像に関連付けられます（例えば、画像のピクセルタイプに対応するマテリアルカタログのカラープロファイル）。

ネストされた画像サービング要求または画像レンダリング要求から得られるマテリアル画像には、通常、カラープロファイルが含まれます。 そうでない場合、画像はピクセルタイプに対応するデフォルトの入力カラースペースに関連付けられます。

画像ファイルのカラースペースが作業用カラースペースと異なる場合は、正確なカラー変換を使用して作業用カラースペースに変換します。 プロファイルが埋め込まれておらず、デフォルトの入力プロファイルが定義されていない場合は、ネイティブタイプの変換が使用されます。

キャビネットスタイルファイル([!DNL .vnc])や窓カバーファイル([!DNL .vnw])など、他のマテリアルデータファイルはカラープロファイルを埋め込まず、常に作業用カラースペースにあると見なされます。

## 出力カラースペース {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

すべてのレンダリング操作は、作業用カラースペースで実行されます。 要求で`icc=`コマンドで別のカラープロファイルを指定した場合、データはエンコードされる直前にそのカラースペースに変換され、クライアントに返されます。 カラーマネジメントが無効な場合、必要に応じて純粋な変換を使用して、グレースケールまたはCMYKに変換します。

## 埋め込みカラープロファイル {#section-5ff733832d38429fbe02b3c1e9bb94a9}

リクエストに対して`iccEmbed=`を指定することで、レンダリングされたイメージに関連付けられたカラープロファイルを応答イメージに埋め込むことができます。

`icc=`を指定しない場合は、作業用カラースペースのICCプロファイルが埋め込まれます。 カラーマネジメントが無効で、`icc=`でプロファイルが指定されていない場合、プロファイルは埋め込まれません。

## ICC プロファイル［ICC ぷろふぁいる］ {#section-afeb76068b5042adb83261638e450140}

サーバーで使用されるすべてのカラープロファイルは、ICC仕様に準拠している必要があります。 ICCプロファイルファイルは通常、[!DNL .icc]または[!DNL .icm]のファイルサフィックスを持ち、マテリアルデータファイルと共に配置されます。

出力プロファイルは`icc=`コマンドでファイルパス/名前で指定できますが、デフォルトのカタログのICCプロファイルマップまたは特定のマテリアルカタログにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカット識別子(`icc::Name`)を使用することをお勧めします。

作業プロファイルは、マテリアルカタログまたはデフォルトカタログのICCプロファイルマップに登録する必要があります。
