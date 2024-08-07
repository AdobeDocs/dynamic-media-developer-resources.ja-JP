---
description: 画像の一部をマスクします。 マスクは常に画像に関連付けられます。 ImageInfo からマスクを取得します。
solution: Experience Manager
title: マスク
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e18096c-0666-400b-a562-b6d183bd3334
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 7%

---

# [!DNL Mask]{#mask}

画像の一部をマスクします。 マスクは常に画像に関連付けられます。 ImageInfo からマスクを取得します。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| maskHandle | `xsd:string` | マスクハンドル。 |
| name | `xsd:string` | マスク名。 |
| maskPath | `xsd:string` | マスクの相対パス。 |
| maskFile | `xsd:string` | ファイルをマスク。 |
| lastModified | `types:dateTime` | マスクが最後に変更された日時およびタイムゾーン。 |
