---
description: サーバーの稼働中は、ファイルが上書きされる直前に req=release コマンドを使用してビネットファイルを置き換えたり、削除したりできます。
solution: Experience Manager
title: ソースデータファイルの削除または置換
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# ソースデータファイルの削除または置換{#deleting-or-replacing-source-data-files}

サーバーの稼働中は、ファイルが上書きされる直前に req=release コマンドを使用してビネットファイルを置き換えたり、削除したりできます。

>[!NOTE]
>
>Render Server がアクセス中は、データファイルを置き換えたり削除したりしないでください。

ソースデータファイルを削除または置き換えると、そのビネットにアクセスする次の要求まで、Render Server はファイルを閉じるだけです。 ファイルを頻繁に使用する場合は、いくつかの再試行が必要になる場合があります。

他のデータファイルを置き換えるには、Render Server を停止する必要があります。

[!DNL Platform Server] マテリアルファイルやビネットを置き換えると、キャッシュエントリは自動的に無効化されます。 ICC プロファイルファイルを置き換えても、キャッシュは無効になりません。

ファイルを置き換える際の複雑な問題を回避するには、置き換えるファイルに新しい名前を付け、対応するカタログエントリを更新することをお勧めします。 これにより、サーバーの稼働中に任意のデータファイルを置き換えることができ、追加の介入なしに、サーバーのキャッシュエントリが自動的に古くなります。 この方法は、画像カタログで管理されるすべてのデータファイルに使用できます。
