---
description: マテリアルカタログには、いくつかのフィーチャがオファーされます。
seo-description: マテリアルカタログには、いくつかのフィーチャがオファーされます。
seo-title: マテリアルカタログ*
solution: Experience Manager
title: マテリアルカタログ*
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# マテリアルカタログ*{#material-catalogs}

マテリアルカタログには、いくつかのフィーチャがオファーされます。

* すべてのマテリアルプロパティを含む、マテリアルの永続的な定義を許可します。

   マテリアルカタログで定義されたマテリアルは、マテリアルプロパティのセットではなく、単純なIDを使用して参照できます。
* JPEG画質やデフォルトの返信画像サイズなど、特定の要求属性のデフォルトを指定します。
* ビネット、ICCプロファイルおよび要求テンプレートを管理します。

特定の材料カタログが定義されていない場合でも、材料カタログのすべてのフィーチャは、既定のカタログ( [!DNL default.ini])を介して使用できます。

レンダリングマテリアルはマテリアル属性を使用する要求で明示的に指定できますが、多くの場合、マテリアルカタログを使用してマテリアルの詳細をWebサイトに表示しない方が望ましいです。 src=コマンドは、明示的なファイルパスの代わりにカタログ参照を受け付けます。 カタログエントリは` [ *[!DNL catId]*/] *[!DNL itemId]*`で構成されます。` *[!DNL catId]*`は材料カタログを、` *[!DNL itemId]*`はカタログ内のレコードを示します。 ` *[!DNL catId]*`を指定しない場合は、セッションカタログが使用されます（以下を参照）。

(a) ` *[!DNL catId]*`が材料カタログの`attribute::RootId`値と一致し、(b) ` *[!DNL recId]*`が同じカタログのcatalog::Id値と一致した場合、カタログレコードは正しく照合されます。 一致が成功した場合、材料の属性（`src=`を含む）はカタログレコードのデータに設定されます。 MSSにsrc=以外のこのマテリアルの追加の属性が含まれる場合は、カタログレコードの値を上書きします。

` *[!DNL recId]*`がカタログエントリと一致しない場合、` *[!DNL catId]*`はカタログから`attribute::RootPath`に置き換えられ、結果のパスは単純なファイルパスと見なされます。 その他のデフォルト属性(`attribute::Resolution`)も材料カタログから継承できます。

ビネットとICCプロファイルは、マテリアルと同様のマテリアルカタログで項目別に分類し、特定のプロパティを指定することができます。 さらに、ビネットマップには、テンプレートのコンテナも表示されます。

**関連項目**

材料カタログ参照， [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
