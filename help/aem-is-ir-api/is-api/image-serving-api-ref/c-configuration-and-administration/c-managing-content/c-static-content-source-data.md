---
description: 静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスされます。
seo-description: 静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスされます。
seo-title: 静的コンテンツソースデータ
solution: Experience Manager
title: 静的コンテンツソースデータ
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 静的コンテンツソースデータ{#static-content-source-data}

静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスされます。

静的コンテンツデータファイルのパスは、次のように解決されます。

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

サーバは、絶対ファイルパスが確立されるまで、右から左へのパスセグメントを結合します。

すべての ` *[!DNL rootPath]*` セグメントは、空、相対または絶対パスセグメントにすることができます。

` *[!DNL catalogPath]*` は、絶対または相対ファイルパス/ファイル名です。 *[!DNL requestPath]* は、相対ファイルパスまたは相対名で指定する必要があります。

で複数 `PS::staticContent.rootPaths` の値を定義できます [!DNL PlatformServer.conf]。 これにより、複数のファイル・システムにソース・データ・ファイルを配布できます。 プラットフォームサーバーは、データファイルが見つかるまで、指定された順序で代替パスを試みます。
