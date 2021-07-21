---
description: 内部でのみ使用します。 ユーザーは、画像サービングの画像カタログの参照 — 属性の参照の節を参照してください。
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

内部でのみ使用します。 ユーザーは、画像サービングの画像カタログの参照 — 属性の参照の節を参照してください。

構文

## 許可されたユーザーの種類 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-79f0d54acd604ad2a5c96679334f2424}

**入力(getImageServingPublishSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 公開設定を画像サービングに設定した会社へのハンドル。 |
| `*`contextHandle`*` | `xsd:string` | はい | パブリッシュコンテキストを処理します。 |

**出力**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | はい | Image Serverの公開設定の配列。 |
