---
description: 内部でのみ使用します。 詳しくは、 [イメージレンダリングマテリアルカタログの参照 — カタログ属性]の節を参照してください。
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 16%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

内部でのみ使用します。 詳しくは、 [イメージレンダリングマテリアルカタログの参照 — カタログ属性]の節を参照してください。

構文

## 許可されたユーザーの種類 {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-4f2cb8c589384816bb2525654ec49963}

**入力(getImageRenderingPublishSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 画像レンダリングの公開設定を取得する会社のハンドル。 |
| `*`contextHandle`*` | `xsd:string` | はい | パブリッシュコンテキストを処理します。 |

**出力(getImageRenderingPublishSettingsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | はい | 画像レンダリングの公開設定 |
