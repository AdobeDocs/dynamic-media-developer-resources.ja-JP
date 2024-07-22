---
description: 指定されたアセットに関連付けられているすべてのビューア設定を取得します。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 20%

---

# getViewerConfigSettings{#getviewerconfigsettings}

指定されたアセットに関連付けられているすべてのビューア設定を取得します。

構文

## 許可されているユーザータイプ {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-7d06abf3d707494c8a1270c7fa1477f1}

**入力（getViewerConfigSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に渡す。 |
| assetHandle | `xsd:string` | はい | アセットへのハンドル。 |

**出力（getViewerCoinfigSettingsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| タイプ | `xsd:string` | はい | 設定が適用されるビューアのタイプ。 |
| configSettingsArray | `types:ConfigSettingsArray` | はい | ビューア設定の配列。 |
