---
title: リソースのルートフォルダー (ir.resourceRootPaths)
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

# リソースのルートフォルダー (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パスまたは次の値を基準とした相対パスを指定できます。 *[!DNL install_folder]*. 複数のパスが指定されている場合、サーバはファイルが見つかるまで、指定された順序で各ルートを試みます。 デフォルトはです。 [!DNL ./resources]（のデフォルトのルートパス） [!DNL install_folder/resources].
