---
description: 静的コンテンツソースデータファイルは、Platform Serverからのみアクセスされます。
solution: Experience Manager
title: 静的コンテンツソースデータ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# 静的コンテンツソースデータ{#static-content-source-data}

静的コンテンツソースデータファイルは、Platform Serverからのみアクセスされます。

静的コンテンツデータファイルのパスは、次のように解決されます。

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

サーバは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべての` *[!DNL rootPath]*`セグメントは、空、相対、または絶対パスセグメントにすることができます。

` *[!DNL catalogPath]*` は、絶対パスまたは相対ファイルパス/名前です。*[!DNL requestPath]* は、相対ファイルパスまたは相対ファイル名にする必要があります。

[!DNL PlatformServer.conf]には複数の`PS::staticContent.rootPaths`値を定義できます。 これにより、ソース・データ・ファイルを複数のファイル・システムに分散できます。 Platform Serverは、データファイルが見つかるまで、指定された順序で代替パスを試みます。
