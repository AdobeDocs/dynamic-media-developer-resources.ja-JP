---
description: 内部でのみ使用します。 詳しくは、「画像レンダリングマテリアルカタログの参照 — カタログ属性」の項を参照してください。
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

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

