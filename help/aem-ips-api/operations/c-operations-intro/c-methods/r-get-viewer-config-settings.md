---
description: 指定したアセットに関連付けられているすべてのビューア設定を取得します。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API，ビューアプリセット
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getViewerConfigSettings{#getviewerconfigsettings}

指定したアセットに関連付けられているすべてのビューア設定を取得します。

構文

## 許可されたユーザーの種類 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-7d06abf3d707494c8a1270c7fa1477f1}

**入力(getViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社に取り扱う。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットに対して処理します。 |

**出力(getViewerConfigSettingsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`type`*` | `xsd:string` | はい | 設定が適用されるビューアタイプ。 |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | はい | ビューア設定の配列。 |
