---
description: マテリアルカタログには、いくつかの機能があります。
seo-description: マテリアルカタログには、いくつかの機能があります。
seo-title: マテリアルカタログ*
solution: Experience Manager
title: マテリアルカタログ*
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# マテリアルカタログ*{#material-catalogs}

マテリアルカタログには、いくつかの機能があります。

* すべての材料特性を含む、材料の永続的な定義を許可します。

   マテリアルカタログで定義されたマテリアルは、マテリアルプロパティのセットではなく、単純なIDを使用して参照できます。
* JPEG画質やデフォルトの返信画像サイズなど、特定の要求属性のデフォルトを指定します。
* ビネット、ICCプロファイル、および要求テンプレートを管理します。

特定の材料カタログが定義されていない場合でも、材料カタログのすべてのフィーチャは、既定のカタログ( [!DNL default.ini])を介して使用できます。

マテリアル属性を使用した要求でレンダリングマテリアルを明示的に指定できますが、多くの場合、マテリアルカタログを使用してマテリアルの詳細をWebサイトに表示しない方が望ましい場合があります。 src=コマンドは、明示的なファイルパスの代わりにカタログ参照を受け付けます。 カタログエントリは、マテリ ` [ *[!DNL catId]*/] *[!DNL itemId]*`アルカタ ` *[!DNL catId]*` ログを識別し、カタ ` *[!DNL itemId]*` ログ内のレコードを識別します。 を指定 ` *[!DNL catId]*` しない場合、セッションカタログが使用されます（以下を参照）。

(a)が材料カタログの値と一致し、(b) ` *[!DNL catId]*` が同じカタ `attribute::RootId` ログのcatalog::Id値と一致する場合、カタログレコードは正しく一致 ` *[!DNL recId]*` します。 一致が成功した場合、マテリアルの属性（を含む）は、カタログレコ `src=`ードのデータに設定されます。 MSSにsrc=以外のこのマテリアルの追加の属性が含まれている場合、カタログ・レコードの値が上書きされます。

カタログ ` *[!DNL recId]*` エントリと一致しない場合、はカ ` *[!DNL catId]*` タログのパ `attribute::RootPath` スに置き換えられ、結果のパスは単純なファイルパスと見なされます。 その他のデフォルト属性(例：)は、マテ `attribute::Resolution`リアルカタログから継承することもできます。

ビネットとICCプロファイルは、マテリアル自体と同様のマテリアルカタログの項目別に表示し、特定のプロパティを指定できます。 さらに、ビネットマップには、テンプレートのコンテナも用意されています。

**関連項目**

マテリアルカタログ [ 参照、、 `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)、、 `attribute::RootId``attribute::RootPath``attribute::VignettePath`
