---
title: 材料カタログ
description: マテリアル カタログには、いくつかの機能があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 材料カタログ {#material-catalogs}

マテリアル カタログには、いくつかの機能があります。

* すべての材料プロパティを含む、材料の永続的な定義を許可します。

  マテリアル カタログで定義されたマテリアルは、マテリアル プロパティのセットではなく、単純な ID を使用して参照できます。
* JPEGの画質やデフォルトの返信画像サイズなど、特定のリクエスト属性のデフォルトを指定します。
* ビネット、ICC プロファイルおよびリクエストテンプレートを管理します。

特定の材料カタログが定義されていない場合でも、材料カタログのすべての機能は既定のカタログ（[!DNL default.ini]）を介して使用できます。

マテリアル属性を使用して要求でレンダリング マテリアルを明示的に指定することもできますが、多くの場合、マテリアル カタログを使用して Web サイトからマテリアルの詳細を非表示にすることをお勧めします。 src= コマンドは、明示的なファイルパスではなくカタログ参照を受け付けます。 カタログ エントリは、` [ *[!DNL catId]*/] *[!DNL itemId]*` で構成されます。ここで、` *[!DNL catId]*` はマテリアル カタログを識別し、` *[!DNL itemId]*` はカタログ内のレコードを識別します。 ` *[!DNL catId]*` を指定しない場合は、セッションカタログが使用されます（以下を参照）。

（a） ` *[!DNL catId]*` が材料カタログの `attribute::RootId` 値と一致し、（b）が同じカタログ内の catalog::Id 値と一致す ` *[!DNL recId]*` 場合、カタログ レコードは正常に照合されます。 正常に一致すると、マテリアルの属性（`src=` を含む）がカタログ レコードのデータに設定されます。 MSS にこのマテリアルの追加の属性が src=以外に含まれている場合、カタログ レコードの値が上書きされます。

` *[!DNL recId]*` をカタログエントリと一致させることができない場合、` *[!DNL catId]*` はカタログの `attribute::RootPath` に置き換えられ、結果のパスは単純なファイルパスと見なされます。 その他の既定の属性（`attribute::Resolution` など）も、マテリアル カタログから継承される場合があります。

ビネットと ICC プロファイルは、マテリアル自体と同様のマテリアル カタログで項目別に分類でき、プロパティを指定できます。 さらに、ビネットマップにはテンプレートのコンテナも含まれています。

**関連トピック**

マテリアル カタログ リファレンス，[`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
