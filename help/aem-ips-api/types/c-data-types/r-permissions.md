---
description: アセットに対するアクセス、変更、作成または削除の権限をグループ別に管理します。
solution: Experience Manager
title: 権限
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---


# 権限{#permission}

アセットに対するアクセス、変更、作成または削除の権限をグループ別に管理します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | グループハンドル |
| `*`groupName`*` | `xsd:string` | グループ名。 |
| `*`permissionType`*` | `xsd:string` | 権限の種類の選択。 |
| `*`isAllowed`*` | `xsd:boolean` | 権限を許可するかどうかを指定します。 |
| `*`isOverride`*` | `xsd:boolean` | 権限が別の権限を上書きするかどうかを指定します。 |

