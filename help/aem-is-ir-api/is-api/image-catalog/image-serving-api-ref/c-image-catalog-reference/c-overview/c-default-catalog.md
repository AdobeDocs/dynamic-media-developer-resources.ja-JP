---
description: デフォルトのカタログは、すべての画像カタログのすべてのカタログ属性のデフォルト値を提供します。
solution: Experience Manager
title: デフォルトのカタログ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# デフォルトのカタログ{#default-catalog}

デフォルトのカタログは、すべての画像カタログのすべてのカタログ属性のデフォルト値を提供します。

特定の属性が特定の画像カタログに見つからない場合、サーバーは代わりに、デフォルトのカタログの対応する値を使用します。 同様に、デフォルトのカタログを使用して、特定のカタログデータレコード（画像、マクロ定義、フォント、ICCプロファイル）のデフォルトを提供できます。 特定のデータレコードが特定の画像カタログに見つからない場合、サーバーは代わりに、デフォルトのカタログで見つけようとします。 これにより、画像カタログをほとんど入力せず、共有テンプレート、マクロ、フォントなどのグローバル属性とデータの管理を簡素化できます。

また、特定の画像カタログが操作に関係しない場合、デフォルトのカタログはすべての属性とデータレコード（マクロ、フォント、ICCプロファイル、リクエスト前処理ルール）を提供します。

Platform Serverを正しく機能させるには、デフォルトのカタログのカタログ属性ファイルに[!DNL default.ini]という名前を付け、常にカタログフォルダーに存在し、`attribute::RootId`を除く必要なすべての属性と、各種カタログデータファイルへの参照（すべてオプション）を完全に設定する必要があります。

>[!NOTE]
>
>[!DNL default.ini]を除くすべてのカタログ属性ファイルには、一意の`attribute::RootId`値が含まれている必要があります。 `attribute::RootId` は空にす [!DNL default.ini] る必要があります。
