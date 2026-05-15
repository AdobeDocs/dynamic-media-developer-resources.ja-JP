---
description: Vignette ファイルは、ファイルが上書きされる直前にreq=release コマンドを使用することで、サーバーの稼働中に置き換えたり削除したりできます。
solution: Experience Manager
title: ソースデータファイルの削除または置換
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
TQID: 'https://experienceleague.adobe.com/clXDwtsKfD4WkpgNvoJoXG19WvFkcOhdjtTGmoArpv4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 0%

---

# ソースデータファイルの削除または置換{#deleting-or-replacing-source-data-files}

Vignette ファイルは、ファイルが上書きされる直前にreq=release コマンドを使用することで、サーバーの稼働中に置き換えたり削除したりできます。

>[!NOTE]
>
>レンダーサーバーがアクセスしている間は、データファイルを置き換えたり削除したりしないでください。

ソースデータファイルを削除または置き換えると、その周辺光量補正にアクセスする次のリクエストまで、レンダーサーバーはファイルを閉じることになります。 ファイルが頻繁に使用されている場合は、数回の再試行が必要になることがあります。

他のデータファイルを置き換えるには、レンダーサーバーを停止する必要があります。

マテリアル ファイルまたはビネットが置き換えられると、[!DNL Platform Server]個のキャッシュ エントリが自動的に無効になります。 ICC プロファイルファイルを置き換えても、キャッシュは無効になりません。

ファイルの置き換えに伴う複雑な作業を避けるために、置き換えファイルに新しい名前を付け、対応するカタログエントリを更新することをお勧めします。 これにより、サーバーの稼働中にデータファイルを置き換えることが可能になり、追加の介入なしでサーバーキャッシュエントリが自動的に古くなります。 この方法は、画像カタログで管理されるすべてのデータファイルに使用できます。
