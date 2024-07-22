---
description: 内部のみで使用します。 Image Rendering Material Catalog Reference-Catalog Attributes セクションを参照してください。
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 16%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

内部のみで使用します。 Image Rendering Material Catalog Reference-Catalog Attributes セクションを参照してください。

構文

## 許可されているユーザータイプ {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-4f2cb8c589384816bb2525654ec49963}

**入力（getImageRenderingPublishSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像レンダリング公開設定を取得する会社のハンドル。 |
| contextHandle | `xsd:string` | はい | 公開コンテキストへのハンドル。 |

**Output （getImageRenderingPublishSettingsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | はい | 画像レンダリングの公開設定。 |
