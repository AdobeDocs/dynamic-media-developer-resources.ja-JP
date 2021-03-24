---
description: 指定したアセットに関連付けられているビューア設定をすべて取得します。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Mediaクラシック，SDK/API，ビューアプリセット
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

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

