---
title: リソース ルート フォルダー（ir.resourceRootPaths）
description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# リソース ルート フォルダー（ir.resourceRootPaths）{#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パス、または *[!DNL install_folder]* に対する相対パスを指定できます。 複数のパスが指定された場合、ファイルが見つかるまで、サーバーは指定された順序で各ルートを試します。 デフォルトは [!DNL ./resources] です。デフォルトのルートパスは [!DNL install_folder/resources] です。
