---
description: SWFビューアの設定を更新します。
seo-description: SWFビューアの設定を更新します。
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
feature: Dynamic Mediaクラシック，SDK/API，ビューアプリセット
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 12%

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
