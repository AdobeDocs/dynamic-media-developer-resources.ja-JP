---
description: ビューア設定をアセットに添付します。 ビューアプリセットまたはビューアのソースアセットを指定できます。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 11%

---


# setViewerConfigSettings{#setviewerconfigsettings}

ビューア設定をアセットに添付します。 ビューアプリセットまたはビューアのソースアセットを指定できます。

構文

## 認証済みユーザータイプ{#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-bcc8c83cc84141e8b1341be9133e8511}

**入力(setViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル |
| `*`name`*` | `xsd:string` | はい | アセット名。 |
| `*`type`*` | `xsd:string` | はい | ビューア設定を適用するアセットのタイプ。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | はい | `ConfigSettings`の配列がアセットに適用されました。 |

**出力(setViewerConfigSettingsParam)**

IPS APIは、この操作に対する応答を返しません。
