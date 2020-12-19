---
description: ビューア設定をアセットに添付します。 ビューアプリセットまたはビューアのソースアセットを指定できます。
seo-description: ビューア設定をアセットに添付します。 ビューアプリセットまたはビューアのソースアセットを指定できます。
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Scene7 Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 10%

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
| ` *`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | アセットハンドル |
| ` *`name`*` | `xsd:string` | はい | アセット名。 |
| ` *`type`*` | `xsd:string` | はい | ビューア設定を適用するアセットのタイプ。 |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | はい | `ConfigSettings`の配列がアセットに適用されました。 |

**出力(setViewerConfigSettingsParam)**

IPS APIは、この操作に対する応答を返しません。
