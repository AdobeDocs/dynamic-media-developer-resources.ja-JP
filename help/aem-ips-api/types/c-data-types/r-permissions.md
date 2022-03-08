---
description: アセットへのアクセス、変更、作成、削除の権限をグループごとに管理します。
solution: Experience Manager
title: 権限
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 9%

---

# 権限{#permission}

アセットへのアクセス、変更、作成、削除の権限をグループごとに管理します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| groupHandle | `xsd:string` | グループハンドル。 |
| groupName | `xsd:string` | グループ名。 |
| permissionType | `xsd:string` | 権限タイプの選択。 |
| isAllowed | `xsd:boolean` | 権限を許可するかどうかを指定します。 |
| isOverride | `xsd:boolean` | 権限が別の権限を上書きするかどうかを指定します。 |
