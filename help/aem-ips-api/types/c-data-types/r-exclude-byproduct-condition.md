---
description: 検索結果から除外する生成エンジンと生成されたアセットタイプを決定します。
solution: Experience Manager
title: ExcludeByproductCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5b37e01b-9e9c-4d34-9d39-1f9bfe356e53
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---

# [!DNL ExcludeByproductCondition]{#excludebyproductcondition}

検索結果から除外する生成エンジンと生成されたアセットタイプを決定します。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 除外するアセットを作成した生成エンジン。 値については、世代情報を参照してください。 |
| generatedAssetType | `xsd:string` | 除外されたアセットタイプ。 値については、アセットタイプを参照してください。 |
