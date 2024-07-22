---
description: ファイルが上書きされる直前に req=release コマンドを使用することで、サーバーの稼働中に Vignette ファイルを置き換えたり削除したりすることができます。
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

ファイルが上書きされる直前に req=release コマンドを使用することで、サーバーの稼働中に Vignette ファイルを置き換えたり削除したりすることができます。

>[!NOTE]
>
>レンダリング サーバがアクセス中は、データ ファイルを置き換えたり削除したりしないでください。

ソース データ ファイルを削除または置換すると、そのビネットにアクセスする次の要求が行われるまで、Render Server はファイルを閉じることに注意してください。 ファイルを頻繁に使用する場合は、再試行が必要になる場合があります。

他のデータファイルを置き換えるには、Render Server を停止する必要があります。

マテリアル ファイルまたはビネットが置き換えられると、[!DNL Platform Server] のキャッシュ エントリは自動的に無効になります。 ICC プロファイルファイルを置き換えても、キャッシュは無効になりません。

ファイルの置き換えの複雑さを避けるために、置き換えるファイルに新しい名前を付け、対応するカタログエントリを更新することをお勧めします。 これにより、サーバーの稼働中にデータファイルを置き換えることができ、追加の介入なしにサーバーキャッシュエントリが自動的に古くなってしまいます。 この方法は、画像カタログで管理されるすべてのデータファイルに使用できます。
