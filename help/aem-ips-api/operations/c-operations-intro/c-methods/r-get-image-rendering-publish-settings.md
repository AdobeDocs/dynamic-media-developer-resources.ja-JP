---
description: 内部でのみ使用します。 詳しくは、画像レンダリングマテリアルカタログの参照 — カタログ属性の節を参照してください。
seo-description: 内部でのみ使用します。 詳しくは、画像レンダリングマテリアルカタログの参照 — カタログ属性の節を参照してください。
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Scene7 Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

内部でのみ使用します。 詳しくは、画像レンダリングマテリアルカタログの参照 — カタログ属性の節を参照してください。

構文

## 認証されたユーザータイプ {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-4f2cb8c589384816bb2525654ec49963}

**入力(getImageRenderingPublishSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 画像レンダリング公開設定を取得する会社のハンドル。 |
| ` *`contextHandle`*` | `xsd:string` | はい | パブリッシュコンテキストの処理。 |

**出力(getImageRenderingPublishSettingsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`publishSettingsArray`*` | `type:ConfigSettingArray` | はい | 画像レンダリングの公開設定 |

