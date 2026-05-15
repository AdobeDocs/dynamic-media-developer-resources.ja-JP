---
description: 静的コンテンツ ソース データ ファイルには、 [!DNL Platform Server]からのみアクセスできます。
solution: Experience Manager
title: 静的なコンテンツソースデータ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# 静的なコンテンツソースデータ{#static-content-source-data}

静的コンテンツ ソース データ ファイルには、[!DNL Platform Server]からのみアクセスできます。

静的コンテンツデータファイルのパスは、次のように解決されます。

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

サーバーは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべての` *[!DNL rootPath]*` セグメントは、空、相対、または絶対パスセグメントにすることができます。

` *[!DNL catalogPath]*`は絶対または相対ファイルパス/名前です。 *[!DNL requestPath]*&#x200B;は相対ファイルパス/名前である必要があります。

複数の`PS::staticContent.rootPaths`値を[!DNL PlatformServer.conf]で定義できます。 これにより、ソースデータファイルを複数のファイルシステムに分散させることができます。 [!DNL Platform Server]は、データファイルが見つかるまで、指定された順序で代替パスを試みます。
