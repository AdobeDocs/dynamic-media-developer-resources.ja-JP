---
description: 内部でのみ使用します。 詳しくは、「画像レンダリングマテリアルカタログの参照 — カタログ属性」の項を参照してください。
seo-description: 内部でのみ使用します。 詳しくは、「画像レンダリングマテリアルカタログの参照 — カタログ属性」の項を参照してください。
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

内部でのみ使用します。 詳しくは、「画像レンダリングマテリアルカタログの参照 — カタログ属性」の項を参照してください。

構文

## 認証済みユーザータイプ{#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-4f2cb8c589384816bb2525654ec49963}

**入力(getImageRenderingPublishSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 画像レンダリング公開設定を取得する会社のハンドル。 |
| `*`contextHandle`*` | `xsd:string` | はい | パブリッシュコンテキストへの処理。 |

**出力(getImageRenderingPublishSettingsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | はい | 画像レンダリングの公開設定 |

