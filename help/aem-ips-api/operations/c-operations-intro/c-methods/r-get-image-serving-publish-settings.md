---
description: 内部でのみ使用します。 ユーザは、「画像サービングの画像カタログ参照 — 属性参照」の節を参照してください。
seo-description: 内部でのみ使用します。 ユーザは、「画像サービングの画像カタログ参照 — 属性参照」の節を参照してください。
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Scene7 Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

内部でのみ使用します。 ユーザは、「画像サービングの画像カタログ参照 — 属性参照」の節を参照してください。

構文

## 認証済みユーザータイプ{#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-79f0d54acd604ad2a5c96679334f2424}

**入力(getImageServingPublishSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 画像サービングの公開設定を含む会社へのハンドル。 |
| ` *`contextHandle`*` | `xsd:string` | はい | パブリッシュコンテキストへの処理。 |

**Output**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`publishSettingArray`*` | `xsd:string` | はい | Image Server公開設定の配列。 |

