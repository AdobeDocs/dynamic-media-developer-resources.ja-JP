---
description: 静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスできます。
seo-description: 静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスできます。
seo-title: 静的コンテンツソースデータ
solution: Experience Manager
title: 静的コンテンツソースデータ
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
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
