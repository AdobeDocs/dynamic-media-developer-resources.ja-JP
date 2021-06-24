---
description: マテリアルカタログは、いくつかの機能を提供します。
solution: Experience Manager
title: マテリアルカタログ*
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# マテリアルカタログ*{#material-catalogs}

マテリアルカタログは、いくつかの機能を提供します。

* すべてのマテリアルプロパティを含む、マテリアルの永続的な定義を許可します。

   マテリアルカタログで定義されたマテリアルは、マテリアルプロパティのセットではなく、単純なIDを使用して参照できます。
* JPEG画質やデフォルトの返信画像サイズなど、特定の要求属性のデフォルトを指定します。
* ビネット、ICCプロファイル、および要求テンプレートを管理します。

特定のマテリアルカタログが定義されていない場合でも、マテリアルカタログのすべてのフィーチャは既定のカタログ( [!DNL default.ini] )を使用して使用できます。

マテリアルは、マテリアル属性を使用した要求で明示的に指定できますが、多くの場合、マテリアルカタログを使用してWebサイトからマテリアルの詳細を非表示にする方が望ましいです。 src=コマンドは、明示的なファイルパスの代わりにカタログ参照を受け付けます。 カタログエントリは` [ *[!DNL catId]*/] *[!DNL itemId]*`で構成されます。ここで、` *[!DNL catId]*`はマテリアルカタログを、` *[!DNL itemId]*`はカタログ内のレコードを表します。 ` *[!DNL catId]*`を指定しない場合は、セッションカタログが使用されます（以下を参照）。

(a) ` *[!DNL catId]*`がマテリアルカタログの`attribute::RootId`値と一致し、(b) ` *[!DNL recId]*`が同じカタログのcatalog::Id値と一致する場合、カタログレコードは正常に照合されます。 一致が成功した場合、マテリアルの属性（`src=`を含む）はカタログレコードのデータに設定されます。 MSSにsrc=以外の追加の属性が含まれている場合、カタログレコードの値を上書きします。

` *[!DNL recId]*`がカタログエントリと一致しない場合、` *[!DNL catId]*`はカタログから`attribute::RootPath`に置き換えられ、結果のパスは単純なファイルパスと見なされます。 その他のデフォルト属性(例：`attribute::Resolution`)は、マテリアルカタログから継承される場合もあります。

ビネットとICCプロファイルは、マテリアル自体に似たマテリアルカタログ、および指定されたプロパティで定義できます。 また、ビネットマップには、テンプレート用のコンテナも用意されています。

**関連項目**

マテリアルカタログ参照、[ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)、`attribute::RootId`、`attribute::RootPath`、`attribute::VignettePath`
