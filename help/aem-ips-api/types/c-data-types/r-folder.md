---
description: 階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。
solution: Experience Manager
title: フォルダ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# フォルダ{#folder}

階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | フォルダーハンドル |
| `*`パス`*` | `xsd:string` | フォルダーのパス。 |
| `*`lastModified`*` | `xsd:dateTime` | 最終変更日。 |
| `*`childLastModified`*` | `xsd:dateTime` | サブフォルダーとフォルダーの子アセットの最終変更日。 |
| `*`permissionsSetHandle`*` | `xsd:string` | フォルダー権限ハンドル。 |
| `*`hasSubfolder`*` | `types:Boolean` | フォルダーにサブフォルダーが含まれているかどうかを指定します。 |
| `*`subfolderArray`*` | `types:FolderArray` | フォルダー内のサブフォルダーの配列です。 |

