---
description: ビューア設定をアセットに添付します。 ビューアプリセットまたはビューアのソースアセットを指定できます。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 11%

---

# setViewerConfigSettings{#setviewerconfigsettings}

ビューア設定をアセットに添付します。 ビューアプリセットまたはビューアのソースアセットを指定できます。

構文

## 許可されているユーザータイプ {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-bcc8c83cc84141e8b1341be9133e8511}

**入力（setViewerConfigSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に渡す。 |
| assetHandle | `xsd:string` | はい | アセットハンドル。 |
| name | `xsd:string` | はい | アセット名。 |
| タイプ | `xsd:string` | はい | ビューア設定を適用するアセットのタイプ。 |
| configSettingArray | `types:ConfigSettingArray` | はい | アセットに適用される `ConfigSettings` の配列。 |

**出力（setViewerConfigSettingsParam）**

IPS API は、この操作に対して応答を返しません。
