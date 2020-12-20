---
description: 画像の一部をマスクします。 マスクは常に画像に関連付けられます。 ImageInfoからマスクを取得します。
seo-description: 画像の一部をマスクします。 マスクは常に画像に関連付けられます。 ImageInfoからマスクを取得します。
seo-title: マスク
solution: Experience Manager
title: マスク
topic: Scene7 Image Production System API
uuid: 06ac0f76-13ce-434b-ac60-6a2af9648f92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 12%

---


# マスク{#mask}

画像の一部をマスクします。 マスクは常に画像に関連付けられます。 ImageInfoからマスクを取得します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`maskHandle`*` | `xsd:string` | マスクハンドル |
| ` *`name`*` | `xsd:string` | マスク名。 |
| ` *`maskPath`*` | `xsd:string` | マスクの相対パス。 |
| ` *`maskFile`*` | `xsd:string` | マスクファイル. |
| ` *`lastModified`*` | `types:dateTime` | マスクが最後に変更された日付、時刻およびタイムゾーン。 |

