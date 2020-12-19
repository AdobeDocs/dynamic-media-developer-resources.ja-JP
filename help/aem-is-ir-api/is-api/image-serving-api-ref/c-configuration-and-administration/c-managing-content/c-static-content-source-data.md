---
description: 静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスできます。
seo-description: 静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスできます。
seo-title: 静的コンテンツソースデータ
solution: Experience Manager
title: 静的コンテンツソースデータ
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# 静的コンテンツソースデータ{#static-content-source-data}

静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスできます。

静的コンテンツデータファイルのパスは、次のように解決されます。

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

サーバは、絶対ファイルパスが確立されるまで、右から左へのパスセグメントを組み合わせます。

すべての` *[!DNL rootPath]*`セグメントは、空、相対、または絶対パスセグメントにすることができます。

` *[!DNL catalogPath]*` は、絶対ファイルパスまたは相対ファイル名です。*[!DNL requestPath]* は、相対ファイルパスまたはファイル名で指定する必要があります。

[!DNL PlatformServer.conf]では複数の`PS::staticContent.rootPaths`値を定義できます。 これにより、ソース・データ・ファイルを複数のファイル・システムに分散できます。 プラットフォームサーバーは、データファイルが見つかるまで、指定された順序で代替パスを試します。
