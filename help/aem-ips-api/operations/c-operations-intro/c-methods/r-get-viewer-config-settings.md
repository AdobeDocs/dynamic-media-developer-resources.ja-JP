---
description: 指定したアセットに関連付けられているビューア設定をすべて取得します。
seo-description: 指定したアセットに関連付けられているビューア設定をすべて取得します。
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
feature: Dynamic Mediaクラシック，SDK/API，ビューアプリセット
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

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

