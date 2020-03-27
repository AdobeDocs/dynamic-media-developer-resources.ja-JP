---
description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-description: セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。
seo-title: リソースルートフォルダ(ir.resourceRootPaths)
solution: Experience Manager
title: リソースルートフォルダ(ir.resourceRootPaths)
topic: Scene7 Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# リソースルートフォルダ(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

セミコロンで区切られたパスのリストは、相対ファイルパスを持つすべてのデータファイルのルートとして機能します。

絶対パスまたは[!DNL *[!DNL install_folder]*]を基準とする相対パスを指定できます。 複数のパスを指定した場合、サーバーは指定された順序で各ルートを試み、ファイルが見つかるまで待ちます。 既定値 [!DNL ./ resources]は、[!DNL *[!DNL install_folder]*/resources]の既定のルートパスです。
