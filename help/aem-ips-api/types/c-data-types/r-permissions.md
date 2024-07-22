---
description: グループごとにアセットへのアクセス、変更、作成、削除の権限を管理します。
solution: Experience Manager
title: 権限
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 7%

---

# [!DNL Permission]{#permission}

グループごとにアセットへのアクセス、変更、作成、削除の権限を管理します。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| groupHandle | `xsd:string` | グループハンドル。 |
| groupName | `xsd:string` | グループ名。 |
| permissionType | `xsd:string` | 権限タイプを選択します。 |
| isAllowed | `xsd:boolean` | 権限が許可されているかどうかを判断します。 |
| isOverride | `xsd:boolean` | 権限が別の権限を上書きするかどうかを決定します。 |
