---
description: サーバーのライブ状態でビネットファイルを置き換えたり、削除したりするには、ファイルが上書きされる直前にreq=releaseコマンドを使用します。
solution: Experience Manager
title: ソースデータファイルの削除または置換
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# ソースデータファイルの削除または置換{#deleting-or-replacing-source-data-files}

サーバーのライブ状態でビネットファイルを置き換えたり、削除したりするには、ファイルが上書きされる直前にreq=releaseコマンドを使用します。

>[!NOTE]
>
>レンダリングサーバーがアクセスしている間は、データファイルを置き換えたり削除したりしないでください。

ソースデータファイルを削除または置き換えると、そのビネットにアクセスする次の要求が発生するまで、Render Serverはファイルを閉じるだけです。 ファイルを頻繁に使用する場合は、いくつかの再試行が必要になる場合があります。

他のデータファイルを置き換えるには、Render Serverを停止する必要があります。

マテリアルファイルやビネットを置き換えると、Platform Serverのキャッシュエントリが自動的に無効化されます。 ICCプロファイルファイルを置き換えても、キャッシュは無効になりません。

ファイルの置き換えに伴う複雑な問題を回避するために、置き換えるファイルに新しい名前を付け、対応するカタログエントリを更新することをお勧めします。 これにより、サーバーが稼動中に任意のデータファイルを置き換えることができ、追加の介入を必要とせずに、サーバーキャッシュエントリが自動的に古くなります。 この方法は、画像カタログで管理されるすべてのデータファイルに使用できます。
