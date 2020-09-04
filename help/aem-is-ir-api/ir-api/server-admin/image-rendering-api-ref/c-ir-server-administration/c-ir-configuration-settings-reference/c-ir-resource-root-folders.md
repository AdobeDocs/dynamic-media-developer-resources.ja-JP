---
description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-title: リソースルートフォルダー(ir.resourceRootPaths)
solution: Experience Manager
title: リソースルートフォルダー(ir.resourceRootPaths)
topic: Scene7 Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 2bc6fe0369808990642cf7afdccff647c48260d9
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# リソースルートフォルダー(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パスまたは相対パスを指定でき *[!DNL install_folder]*&#x200B;ます。 複数のパスを指定した場合、サーバは指定された順序で各ルートを試み、ファイルが見つかるまで待ちます。 初期設定はで [!DNL ./resources]、のデフォルトのルートパス [!DNL install_folder/resources]です。
