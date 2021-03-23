---
description: 階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。
seo-description: 階層ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。
seo-title: フォルダ
solution: Experience Manager
title: フォルダ
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

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

