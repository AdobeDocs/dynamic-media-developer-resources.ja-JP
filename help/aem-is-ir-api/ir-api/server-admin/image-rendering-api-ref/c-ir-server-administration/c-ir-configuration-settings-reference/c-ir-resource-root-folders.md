---
description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
solution: Experience Manager
title: リソースルートフォルダー(ir.resourceRootPaths)
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# リソースルートフォルダー(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスを指定できます。 複数のパスを指定した場合、サーバーはファイルが見つかるまで、指定された順序で各ルートを試みます。 デフォルトは[!DNL ./resources]で、デフォルトのルートパスは[!DNL install_folder/resources]です。
