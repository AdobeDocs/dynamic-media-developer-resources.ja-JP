---
description: 階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。
solution: Experience Manager
title: フォルダ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# フォルダ{#folder}

階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | フォルダーハンドル。 |
| `*`パス`*` | `xsd:string` | フォルダーパス。 |
| `*`lastModified`*` | `xsd:dateTime` | 最終変更日。 |
| `*`childLastModified`*` | `xsd:dateTime` | サブフォルダーおよびフォルダーの子アセットの最終変更日。 |
| `*`permissionsSetHandle`*` | `xsd:string` | フォルダー権限ハンドル。 |
| `*`hasSubfolder`*` | `types:Boolean` | フォルダーにサブフォルダーがあるかどうかを指定します。 |
| `*`subfolderArray`*` | `types:FolderArray` | フォルダー内のサブフォルダーの配列。 |
