---
description: 指定したアセットに関連付けられているすべてのビューア設定を取得します。
seo-description: 指定したアセットに関連付けられているすべてのビューア設定を取得します。
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Scene7 Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getViewerConfigSettings{#getviewerconfigsettings}

指定したアセットに関連付けられているすべてのビューア設定を取得します。

構文

## 認証されたユーザータイプ {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-7d06abf3d707494c8a1270c7fa1477f1}

**入力(getViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の取り扱い。 |
| ` *`assetHandle`*` | `xsd:string` | はい | アセットの処理。 |

**出力(getViewerConfigSettingsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`type`*` | `xsd:string` | はい | 設定を適用するビューアタイプ。 |
| ` *`configSettingsArray`*` | `types:ConfigSettingsArray` | はい | ビューア設定の配列。 |

