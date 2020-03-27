---
description: アセットに対するアクセス、変更、作成または削除の権限をグループ別に管理します。
seo-description: アセットに対するアクセス、変更、作成または削除の権限をグループ別に管理します。
seo-title: 権限
solution: Experience Manager
title: 権限
topic: Scene7 Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Permission{#permission}

アセットに対するアクセス、変更、作成または削除の権限をグループ別に管理します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | グループハンドル。 |
| ` *`groupName`*` | `xsd:string` | グループ名。 |
| ` *`permissionType`*` | `xsd:string` | 権限タイプの選択。 |
| ` *`isAllowed`*` | `xsd:boolean` | 権限を許可するかどうかを指定します。 |
| ` *`isOverride`*` | `xsd:boolean` | 権限が別の権限を上書きするかどうかを指定します。 |

