---
description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
solution: Experience Manager
title: リソースルートフォルダー(ir.resourceRootPaths)
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# リソースルートフォルダー(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;を基準とする相対パスを指定できます。 複数のパスを指定した場合、サーバは指定された順序で各ルートを試み、ファイルが見つかるまで待ちます。 初期設定は[!DNL ./resources]で、デフォルトのルートパスは[!DNL install_folder/resources]です。
