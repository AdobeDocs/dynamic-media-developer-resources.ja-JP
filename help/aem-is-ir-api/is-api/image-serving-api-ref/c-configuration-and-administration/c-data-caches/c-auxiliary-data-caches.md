---
description: ネストされた埋め込み画像サービングおよび画像レンダリングリクエストによって生成された中間画像データは、ネストされた埋め込みリクエストで cache=on を指定することでキャッシュできます。 このデータは、応答データキャッシュ内に独自の形式で保存されます。
solution: Experience Manager
title: 補助データキャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 補助データキャッシュ{#auxiliary-data-caches}

ネストされた埋め込み画像サービングおよび画像レンダリングリクエストによって生成された中間画像データは、ネストされた埋め込みリクエストで cache=on を指定することでキャッシュできます。 このデータは、応答データキャッシュ内に独自の形式で保存されます。

外部 HTTP サーバーから取得された画像も、応答データキャッシュに保存されます。 このような画像は、キャッシュエントリが生成される前に、検証ユーティリティによって自動的に検証されます。

[!DNL Platform Server] は、効率的にアクセスできるよう画像カタログデータをコンパイルします。 このデータは `CS::CatalogCacheFolder` に保存されます。
