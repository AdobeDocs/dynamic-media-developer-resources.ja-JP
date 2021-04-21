---
description: SWFビューアの設定を更新します。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 13%

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

SWFビューアの設定を更新します。

構文

## 認証済みユーザータイプ{#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-29790d933fb24aa392d0cb2d52d1310f}

**入力(updateViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | はい | ビューアに適用する設定の配列。 |

**出力(updateViewerConfigSettingsReturn)**

IPS APIは、この操作に対する応答を返しません。
