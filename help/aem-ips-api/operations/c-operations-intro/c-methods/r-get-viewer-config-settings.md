---
description: 指定したアセットに関連付けられているビューア設定をすべて取得します。
seo-description: 指定したアセットに関連付けられているビューア設定をすべて取得します。
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 18%

---


# getViewerConfigSettings{#getviewerconfigsettings}

指定したアセットに関連付けられているビューア設定をすべて取得します。

構文

## 認証済みユーザータイプ{#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-7d06abf3d707494c8a1270c7fa1477f1}

**入力(getViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットのハンドル。 |

**出力(getViewerConfigSettingsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`type`*` | `xsd:string` | はい | 設定が適用されるビューアタイプ。 |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | はい | ビューア設定の配列。 |

