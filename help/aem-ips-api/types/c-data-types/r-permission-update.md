---
description: 権限の変更を記述します。
solution: Experience Manager
title: PermissionUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a21b9d66-14bd-4983-9eb9-54ab1be1261e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '33'
ht-degree: 15%

---

# [!DNL PermissionUpdate]{#permissionupdate}

権限の変更を記述します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| groupHandle | `xsd:string` | グループハンドル。 |
| permissionType | `xsd:string` | 権限タイプ。 |
| isAllowed | `xsd:boolean` | 権限の更新を許可するかどうかを指定します。 |
| isOverride | `xsd:boolean` | 権限が別の権限を上書きするかどうかを指定します。 |
