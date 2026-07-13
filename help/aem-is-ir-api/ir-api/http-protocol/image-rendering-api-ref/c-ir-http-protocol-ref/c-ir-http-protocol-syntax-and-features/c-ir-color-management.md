---
description: 画像レンダリングは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。
solution: Experience Manager
title: 画像レンダリングのカラーマネジメント *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
TQID: 'https://experienceleague.adobe.com/jreocUOYeYBrId4tPQljML7YhWzxf10tefkkuXONlf4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 741
ht-degree: 0%

---

# 画像レンダリングのカラーマネジメント *{#image-rendering-color-management}

画像レンダリングは、ICC （International Color Consortium）仕様に準拠したカラースペースプロファイルに基づくカラースペース変換をサポートしています。

**制限**

現時点では、CMYK、RGB、およびグレースケールのカラースペースのみがサポートされています。

キャビネット スタイル ファイル（.vnc）とウィンドウ カバレッジ スタイル ファイル（[!DNL .vnw]）はカラーマネジメントされず、作業用カラースペースに存在すると見なされます。

**関連項目**

[国際カラーコンソーシアム ](https://www.color.org/index.xalter)、[`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)、[`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)、`attribute::IccProfile*`、`attribute::IccProfileSrc*`、`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`、`attribute::IccDither`、ICC プロファイルマップ

## デフォルトのカラースペース {#section-8ce27edf42e746febe4654f8f19b9c0c}

各画像カタログ（およびデフォルトのカタログ）は、ICC プロファイルのセットを定義できます。 これらのプロファイルは、このカタログのデフォルトのカラースペースを構成します。それぞれ、グレースケール、RGB、CMYK データ（`attribute::IccProfileRgb`、`attribute::IccProfileGray`、`attribute::IccProfileCmyk`、`attribute::IccProfileSrcRgb`、`attribute::IccProfileSrcGray`、および`attribute::IccProfileSrcCmyk`）用の1つの入力プロファイルと1つの出力プロファイルです。

カタログのデフォルトプロファイルから、画像のピクセルタイプに基づいて、特定の画像または他のオブジェクトのデフォルトカラースペースが選択されます。

## 入力カラースペース {#section-660f661a7e954df4b451e34134195276}

マテリアル画像は、ICC プロファイルを埋め込んで、入力カラースペースを定義できます。 ソース画像にプロファイルが埋め込まれていない場合は、ソース画像のピクセルタイプに対応する該当する画像カタログの`attribute::IccProfileSrc*`が使用されます。 この属性が画像カタログで定義されていない場合は、`attribute::IccProfile*`が使用されます。 カタログ属性が定義されていない場合、画像はカラーマネジメントされず、単純な変換のみが適用されます。

## 作業用カラースペース {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常、作業用カラースペースは、ビネットに埋め込まれたICC カラープロファイルによって定義されます。 ビネットにプロファイルが含まれていない場合、作業用カラースペースにはデフォルトのRGB入力プロファイル（セッションカタログの`attribute::IccProfileSrcRgb`）が使用されます。

すべてのレンダリング操作は、作業用カラースペースで実行されます。

**重要：**&#x200B;作業用カラースペースのICC プロファイルは、入出力変換をサポートしている必要があります。 出力専用プロファイルが作業用カラースペースとして使用されている場合、IRはマテリアルを変換できません。 このようなカラープロファイルは、同じ作業用カラースペースにマテリアルが存在する場合でも使用できます。 他のカラースペースでマテリアルを適用しようとすると、失敗します。

## 明示的なカラー値 {#section-31727bf1b23e477ca92572fbbf422d2f}

`color=`、`bgc=`、`catalog::BgColor`、`catalog::Color`で指定されたRGB カラー値は、現在の作業用カラースペースに存在すると見なされます。

## マテリアルデータファイル {#section-33f7a170a6664c02b8479fb89cc0aea3}

マテリアル画像ファイル（テクスチャ画像およびデカール画像）には、RGB、グレースケール、またはCMYK ピクセルタイプを指定でき、カラープロファイルを埋め込むことができます。 カラープロファイルが埋め込まれていない場合、デフォルトの入力カラースペースは画像に関連付けられます（例えば、画像のピクセルタイプに対応するマテリアルカタログのカラープロファイルなど）。

ネストされた画像サービングまたは画像レンダリング要求から取得されるマテリアル画像には、通常、カラープロファイルが含まれます。 そうでない場合、画像はピクセルタイプに対応するデフォルトの入力カラースペースに関連付けられます。

画像ファイルのカラースペースが作業用カラースペースと異なる場合は、正確な色変換を使用して作業用カラースペースに変換します。 プロファイルが埋め込まれておらず、デフォルトの入力プロファイルが定義されていない場合は、ナイーブ型変換が使用されます。

キャビネット スタイル ファイル （[!DNL .vnc]）やウィンドウ カバーファイル （[!DNL .vnw]）などの他のマテリアル データ ファイルは、カラープロファイルを埋め込むことはなく、常に作業用カラースペースにあると見なされます。

## 出力カラースペース {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

レンダリング操作はすべて、作業用カラースペースで行われます。 リクエストで`icc=` コマンドを使用して別のカラープロファイルを指定した場合、データはエンコードされる直前にそのカラースペースに変換され、クライアントに返されます。 カラーマネジメントが無効になっている場合、必要に応じてネイティブ変換を使用してグレースケールまたはCMYKに変換します。

## 埋め込みカラープロファイル {#section-5ff733832d38429fbe02b3c1e9bb94a9}

レンダリングされた画像に関連付けられているカラープロファイルは、リクエストに`iccEmbed=`を指定することで、応答画像に埋め込むことができます。

`icc=`が指定されていない場合、作業用カラースペースのICC プロファイルが埋め込まれます。 カラーマネジメントが無効になっていて、`icc=`でプロファイルが指定されていない場合、プロファイルは埋め込まれません。

## ICC プロファイル［ICC ぷろふぁいる］ {#section-afeb76068b5042adb83261638e450140}

サーバーが使用するすべてのカラープロファイルは、ICC仕様に準拠している必要があります。 ICC プロファイル ファイルには通常、[!DNL .icc]または[!DNL .icm]個のファイル サフィックスが含まれており、マテリアル データ ファイルと同じ場所にあります。

出力プロファイルは、`icc=` コマンドでファイルパスまたは名前で指定できますが、デフォルトカタログまたは特定のマテリアルカタログのICC プロファイルマップにすべてのプロファイルファイルを登録し、ファイルパスの代わりにショートカット識別子（`icc::Name`）を使用することをお勧めします。

作業プロファイルは、材料カタログまたはデフォルトカタログのICC プロファイルマップに登録する必要があります。

