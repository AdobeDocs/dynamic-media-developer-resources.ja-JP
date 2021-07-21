---
description: SWFビューアの設定を更新します。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API，ビューアプリセット
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 13%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

SWFビューアの設定を更新します。

構文

## 許可されたユーザーの種類 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-29790d933fb24aa392d0cb2d52d1310f}

**入力(updateViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社に取り扱う。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | はい | ビューアに適用する設定の配列。 |

**出力(updateViewerConfigSettingsReturn)**

IPS APIは、この操作に対する応答を返しません。
