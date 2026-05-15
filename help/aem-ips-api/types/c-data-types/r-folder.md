---
description: 階層型ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。
solution: Experience Manager
title: フォルダ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 7%

---

# [!DNL Folder]{#folder}

階層型ファイルまたはアセットストレージオブジェクト。 フォルダーには、1つ以上のサブフォルダーを含めることができます。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| folderHandle | `xsd:string` | フォルダーハンドル。 |
| [!DNL path] | `xsd:string` | フォルダーパス： |
| lastModified | `xsd:dateTime` | 最終変更日。 |
| childLastModified | `xsd:dateTime` | サブフォルダーとフォルダーの子アセットの最終変更日。 |
| permissionsSetHandle | `xsd:string` | フォルダー権限ハンドル。 |
| hasSubfolder | `types:Boolean` | フォルダーにサブフォルダーがあるかどうかを指定します。 |
| subfolderArray | `types:FolderArray` | フォルダー内のサブフォルダーの配列。 |
