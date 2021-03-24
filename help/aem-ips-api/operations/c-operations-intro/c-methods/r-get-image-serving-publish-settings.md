---
description: 内部でのみ使用します。 ユーザは、「画像サービングの画像カタログ参照 — 属性参照」の節を参照してください。
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 14%

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
| `*`companyHandle`*` | `xsd:string` | はい | 画像サービングの公開設定を含む会社へのハンドル。 |
| `*`contextHandle`*` | `xsd:string` | はい | パブリッシュコンテキストへの処理。 |

**Output**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | はい | Image Server公開設定の配列。 |

