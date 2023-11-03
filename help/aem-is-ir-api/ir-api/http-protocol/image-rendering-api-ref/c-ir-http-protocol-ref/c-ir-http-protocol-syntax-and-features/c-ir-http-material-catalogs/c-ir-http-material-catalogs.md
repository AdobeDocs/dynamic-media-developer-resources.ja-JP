---
title: マテリアルカタログ
description: マテリアルカタログは、いくつかの機能を提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# マテリアルカタログ {#material-catalogs}

マテリアルカタログは、いくつかの機能を提供します。

* すべての材料プロパティを含む、材料の永続的な定義を許可します。

  マテリアルカタログで定義されたマテリアルは、マテリアルプロパティのセットではなく、単純な ID を使用して参照できます。
* 特定の要求属性のデフォルト値 (JPEGの質やデフォルトの返信画像サイズなど ) を指定します。
* ビネット、ICC プロファイル、要求テンプレートを管理します。

特定のマテリアルカタログが定義されていない場合でも、マテリアルカタログのすべてのフィーチャは、既定のカタログ ( [!DNL default.ini]) をクリックします。

レンダリングマテリアルは、マテリアル属性を使用した要求で明示的に指定できますが、多くの場合、マテリアルカタログを使用して Web サイトからマテリアルの詳細を非表示にする方が望ましいです。 src=コマンドは、明示的なファイルパスの代わりにカタログ参照を受け付けます。 カタログエントリは、 ` [ *[!DNL catId]*/] *[!DNL itemId]*`です。 ` *[!DNL catId]*` マテリアルカタログを識別し、 ` *[!DNL itemId]*` は、カタログ内のレコードを識別します。 次の場合 ` *[!DNL catId]*` が指定されていない場合、セッションカタログが使用されます（以下を参照）。

(a) の場合、カタログレコードは正常に照合されます。 ` *[!DNL catId]*` が `attribute::RootId` 素材カタログの値と (b) ` *[!DNL recId]*` は、同じカタログ内の catalog::Id 値と一致します。 一致が成功した場合、マテリアルの属性 ( `src=`) がカタログレコードのデータに設定されます。 MSS に src=以外の追加の属性が含まれている場合は、カタログレコードの値を上書きします。

次の場合 ` *[!DNL recId]*` は、カタログエントリに一致しない場合、 ` *[!DNL catId]*` は次の値に置き換えられます。 `attribute::RootPath` カタログから取得され、生成されるパスは単純なファイルパスと見なされます。 その他のデフォルト属性 ( 例： `attribute::Resolution`) は、マテリアルカタログから継承される場合もあります。

ビネットと ICC プロファイルは、マテリアル自体と同様に、マテリアルカタログで項目別に定義し、プロパティを指定することができます。 さらに、ビネットマップには、テンプレート用のコンテナも用意されています。

**関連項目**

マテリアルカタログ参照 [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
