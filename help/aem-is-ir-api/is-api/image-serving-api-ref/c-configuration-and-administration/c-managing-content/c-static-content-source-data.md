---
description: 静的コンテンツソースデータファイルには、 [!DNL Platform Server].
solution: Experience Manager
title: 静的コンテンツソースデータ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# 静的コンテンツソースデータ{#static-content-source-data}

静的コンテンツソースデータファイルには、 [!DNL Platform Server].

静的コンテンツデータファイルのパスは、次のように解決されます。

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

サーバは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべて ` *[!DNL rootPath]*` セグメントは、空、相対または絶対パスセグメントのいずれかです。

` *[!DNL catalogPath]*` は、絶対または相対ファイルパス/名前です。 *[!DNL requestPath]* は、相対ファイルパスまたはファイル名である必要があります。

複数 `PS::staticContent.rootPaths` の値は、 [!DNL PlatformServer.conf]. これにより、ソース・データ・ファイルを複数のファイル・システムに分散させることができます。 この [!DNL Platform Server] は、データファイルが見つかるまで、指定された順序で代替パスを試みます。
