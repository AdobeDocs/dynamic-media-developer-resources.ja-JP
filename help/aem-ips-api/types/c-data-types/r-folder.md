---
description: 階層ファイルまたはアセットストレージオブジェクト。 フォルダには、1つ以上のサブフォルダを含めることができます。
seo-description: 階層ファイルまたはアセットストレージオブジェクト。 フォルダには、1つ以上のサブフォルダを含めることができます。
seo-title: フォルダ
solution: Experience Manager
title: フォルダ
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# フォルダ{#folder}

階層ファイルまたはアセットストレージオブジェクト。 フォルダには、1つ以上のサブフォルダを含めることができます。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | フォルダハンドル |
| ` *`パス`*` | `xsd:string` | フォルダーのパス。 |
| ` *`lastModified`*` | `xsd:dateTime` | 最終変更日。 |
| ` *`childLastModified`*` | `xsd:dateTime` | サブフォルダーとフォルダーの子アセットの最終変更日。 |
| ` *`permissionsSetHandle`*` | `xsd:string` | フォルダ権限ハンドル |
| ` *`hasSubfolder`*` | `types:Boolean` | フォルダーにサブフォルダーが含まれているかどうかを判定します。 |
| ` *`subfolderArray`*` | `types:FolderArray` | フォルダー内のサブフォルダーの配列。 |

