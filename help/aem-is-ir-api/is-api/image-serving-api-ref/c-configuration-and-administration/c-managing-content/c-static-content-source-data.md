---
description: 静的コンテンツソースファイルにアクセスできるのは、 [!DNL Platform Server] のみです。
solution: Experience Manager
title: 静的コンテンツソースデータ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 静的コンテンツソースデータ{#static-content-source-data}

静的コンテンツソースファイルには、[!DNL Platform Server] でのみアクセスできます。

静的コンテンツデータファイルのパスは、次のように解決されます。

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

サーバは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべての ` *[!DNL rootPath]*` セグメントは、空、相対または絶対パスセグメントにすることができます。

` *[!DNL catalogPath]*` は、絶対または相対のファイルパスまたは名前です。 *[!DNL requestPath]* は、相対ファイルパスまたはファイル名である必要があります。

[!DNL PlatformServer.conf] では、複数の `PS::staticContent.rootPaths` 値を定義できます。 これにより、ソース・データ・ファイルを複数のファイル・システムに分散させることができます。 [!DNL Platform Server] は、データファイルが見つかるまで、指定された順序で代替パスを試みます。
