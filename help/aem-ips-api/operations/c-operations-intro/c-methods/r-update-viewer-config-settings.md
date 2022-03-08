---
description: SWFビューアの設定を更新します。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

SWFビューアの設定を更新します。

構文

## 認証済みユーザータイプ {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-29790d933fb24aa392d0cb2d52d1310f}

**入力 (updateViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に対する取り扱い。 |
| assetHandle | `xsd:string` | はい | アセットハンドル。 |
| configSettingArray | `types:ConfigSettingArray` | はい | ビューアに適用する設定の配列。 |

**出力 (updateViewerConfigSettingsReturn)**

IPS API はこの操作に対する応答を返しません。
