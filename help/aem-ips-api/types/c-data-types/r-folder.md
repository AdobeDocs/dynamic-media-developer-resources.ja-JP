---
description: 階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1 つ以上のサブフォルダーを含めることができます。
solution: Experience Manager
title: フォルダ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---

# [!DNL Folder]{#folder}

階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1 つ以上のサブフォルダーを含めることができます。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| folderHandle | `xsd:string` | フォルダーハンドル。 |
| [!DNL path] | `xsd:string` | フォルダーパス。 |
| lastModified | `xsd:dateTime` | 最終変更日。 |
| childLastModified | `xsd:dateTime` | サブフォルダーとフォルダーの子アセットの最終変更日。 |
| permissionsSetHandle | `xsd:string` | フォルダー権限ハンドル。 |
| hasSubfolder | `types:Boolean` | フォルダーにサブフォルダーがあるかどうかを判断します。 |
| subfolderArray | `types:FolderArray` | フォルダーのサブフォルダーの配列。 |
