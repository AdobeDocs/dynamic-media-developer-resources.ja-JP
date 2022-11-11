---
description: ネスト/埋め込みの画像サービング要求および画像レンダリング要求で生成される中間画像データは、ネスト/埋め込み要求で cache=on を指定することでキャッシュできます。 このデータは、応答データキャッシュ内の独自の形式で保存されます。
solution: Experience Manager
title: 補助的なデータキャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 補助的なデータキャッシュ{#auxiliary-data-caches}

ネスト/埋め込みの画像サービング要求および画像レンダリング要求で生成される中間画像データは、ネスト/埋め込み要求で cache=on を指定することでキャッシュできます。 このデータは、応答データキャッシュ内の独自の形式で保存されます。

外部 HTTP サーバーから取得した画像も、応答データキャッシュに保存されます。 このような画像は、キャッシュエントリが生成される前に、検証ユーティリティで自動的に検証されます。

この [!DNL Platform Server] 効率的なアクセスのために画像カタログデータをコンパイルします。 このデータは、 `CS::CatalogCacheFolder`.
