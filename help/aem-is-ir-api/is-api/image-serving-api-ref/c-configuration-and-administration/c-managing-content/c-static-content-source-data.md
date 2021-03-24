---
description: 静的コンテンツソースのデータファイルは、プラットフォームサーバーからのみアクセスできます。
solution: Experience Manager
title: 静的コンテンツソースデータ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
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
