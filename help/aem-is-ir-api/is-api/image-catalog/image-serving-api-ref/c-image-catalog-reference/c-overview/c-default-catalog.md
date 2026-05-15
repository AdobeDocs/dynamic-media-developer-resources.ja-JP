---
description: デフォルトカタログは、すべての画像カタログのすべてのカタログ属性にデフォルト値を提供します。
solution: Experience Manager
title: デフォルトカタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# デフォルトカタログ{#default-catalog}

デフォルトカタログは、すべての画像カタログのすべてのカタログ属性にデフォルト値を提供します。

特定の画像カタログに特定の属性が見つからない場合、サーバーは代わりにデフォルトカタログの対応する値を使用します。 同様に、デフォルトカタログを使用して、特定のカタログデータレコード（画像、マクロ定義、フォント、ICC プロファイル）のデフォルトを指定できます。 特定の画像カタログに特定のデータレコードが見つからない場合、サーバーは代わりにデフォルトカタログで特定のデータレコードを検索しようとします。 これにより、画像カタログの入力が過剰におこなわれなくなり、共有テンプレート、マクロ、フォントなどのグローバル属性やデータの管理が簡素化されます。

さらに、デフォルトのカタログでは、特定の画像カタログが操作に関与していない場合、すべての属性とデータレコード（マクロ、フォント、ICC プロファイル、リクエスト前処理ルール）が提供されます。

[!DNL Platform Server]を正しく機能させるには、既定のカタログのカタログ属性ファイルの名前を[!DNL default.ini]とし、常にカタログフォルダーに存在し、`attribute::RootId`と様々なカタログデータファイルへの参照を除くすべての必要な属性を完全に入力する必要があります。すべてオプションです。

>[!NOTE]
>
>[!DNL default.ini]を除くすべてのカタログ属性ファイルには、一意の`attribute::RootId`値を含める必要があります。 [!DNL default.ini]の`attribute::RootId`は空である必要があります。
