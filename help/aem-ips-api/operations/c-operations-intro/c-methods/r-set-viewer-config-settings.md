---
description: ビューアの設定をアセットにアタッチします。 ビューアプリセットまたはビューアのソースアセットを指定できます。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API，ビューアプリセット
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 11%

---

# setViewerConfigSettings{#setviewerconfigsettings}

ビューアの設定をアセットにアタッチします。 ビューアプリセットまたはビューアのソースアセットを指定できます。

構文

## 許可されたユーザーの種類 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-bcc8c83cc84141e8b1341be9133e8511}

**入力(setViewerConfigSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社に取り扱う。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル。 |
| `*`name`*` | `xsd:string` | はい | アセット名。 |
| `*`type`*` | `xsd:string` | はい | ビューア設定を適用するアセットのタイプ。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | はい | `ConfigSettings`の配列がアセットに適用されています。 |

**出力(setViewerConfigSettingsParam)**

IPS APIは、この操作に対する応答を返しません。
