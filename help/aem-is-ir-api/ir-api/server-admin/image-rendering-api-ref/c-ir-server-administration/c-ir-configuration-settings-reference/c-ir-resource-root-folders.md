---
description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-title: リソースルートフォルダー(ir.resourceRootPaths)
solution: Experience Manager
title: リソースルートフォルダー(ir.resourceRootPaths)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# リソースルートフォルダー(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;を基準とする相対パスを指定できます。 複数のパスを指定した場合、サーバは指定された順序で各ルートを試み、ファイルが見つかるまで待ちます。 初期設定は[!DNL ./resources]で、デフォルトのルートパスは[!DNL install_folder/resources]です。
