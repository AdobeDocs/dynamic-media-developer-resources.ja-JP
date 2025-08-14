---
description: SWF ビューア設定を更新します。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 13%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

SWF ビューア設定を更新します。

構文

## 許可されているユーザータイプ {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-29790d933fb24aa392d0cb2d52d1310f}

**入力（updateViewerConfigSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に渡す。 |
| assetHandle | `xsd:string` | はい | アセットハンドル。 |
| configSettingArray | `types:ConfigSettingArray` | はい | ビューアに適用する設定の配列。 |

**Output （updateViewerConfigSettingsReturn）**

IPS API は、この操作に対して応答を返しません。
