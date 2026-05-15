---
title: マテリアルカタログ
description: マテリアルカタログにはいくつかの機能があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
TQID: 'https://experienceleague.adobe.com/0ALFMea9A1hJtuPr3vG0cd34S-cLfTUNUGpIXZBpZBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 0%

---

# マテリアルカタログ {#material-catalogs}

マテリアルカタログにはいくつかの機能があります。

* すべての材料特性を含め、材料の永続的な定義を許可します。

  マテリアル カタログで定義されたマテリアルは、マテリアル プロパティのセットではなく、単純なIDを使用して参照できます。
* JPEGの画質やデフォルトの返信画像サイズなど、特定のリクエスト属性のデフォルトを指定します。
* 周辺光量補正、ICC プロファイル、リクエストテンプレートを管理します。

特定のマテリアル カタログが定義されていない場合でも、マテリアル カタログのすべての機能は、既定のカタログ（[!DNL default.ini]）を介して利用できます。

マテリアル属性を使用してリクエストでレンダリング マテリアルを明示的に指定する場合がありますが、多くの場合、マテリアル カタログを使用してweb サイトからマテリアルの詳細を非表示にすることをお勧めします。 src= コマンドは、明示的なファイルパスの代わりにカタログ参照を受け入れます。 カタログ エントリは` [ *[!DNL catId]*/] *[!DNL itemId]*`で構成され、` *[!DNL catId]*`はマテリアル カタログを識別し、` *[!DNL itemId]*`はカタログ内のレコードを識別します。 ` *[!DNL catId]*`が指定されていない場合は、セッションカタログが使用されます（以下を参照）。

（a） ` *[!DNL catId]*`がマテリアルカタログの`attribute::RootId`値と一致し、（b） ` *[!DNL recId]*`が同じカタログのcatalog::Id値と一致する場合、カタログレコードは正常に照合されます。 一致が成功した場合、マテリアルの属性（`src=`を含む）は、カタログ レコードのデータに設定されます。 MSSにsrc=以外にこのマテリアルの追加の属性が含まれる場合、カタログレコードの値を上書きします。

` *[!DNL recId]*`をカタログ エントリに一致させることができない場合、` *[!DNL catId]*`はカタログから`attribute::RootPath`に置き換えられ、結果のパスは単純なファイル パスと見なされます。 その他の既定の属性（例：`attribute::Resolution`）も、マテリアル カタログから継承できます。

ビネットとICC プロファイルは、マテリアル自体と同様にマテリアル カタログに列挙し、プロパティを指定できます。 さらに、周辺光量補正マップには、テンプレート用のコンテナも用意されています。

**関連項目**

マテリアル カタログ参照、[`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)、`attribute::RootId`、`attribute::RootPath`、`attribute::VignettePath`
