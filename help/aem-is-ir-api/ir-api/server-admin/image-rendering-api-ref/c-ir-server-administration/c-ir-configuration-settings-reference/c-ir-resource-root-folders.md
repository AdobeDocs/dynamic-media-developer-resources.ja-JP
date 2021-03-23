---
description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-title: リソースルートフォルダー(ir.resourceRootPaths)
solution: Experience Manager
title: リソースルートフォルダー(ir.resourceRootPaths)
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# リソースルートフォルダー(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;を基準とする相対パスを指定できます。 複数のパスを指定した場合、サーバは指定された順序で各ルートを試み、ファイルが見つかるまで待ちます。 初期設定は[!DNL ./resources]で、デフォルトのルートパスは[!DNL install_folder/resources]です。
