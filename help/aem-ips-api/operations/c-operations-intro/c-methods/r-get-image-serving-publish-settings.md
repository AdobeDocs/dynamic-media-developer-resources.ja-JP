---
description: 内部でのみ使用します。 ユーザーは、画像サービングの画像カタログ参照 — 属性リファレンスの節を参照してください。
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

内部でのみ使用します。 ユーザーは、画像サービングの画像カタログ参照 — 属性リファレンスの節を参照してください。

構文

## 認証済みユーザータイプ {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-79f0d54acd604ad2a5c96679334f2424}

**入力 (getImageServingPublishSettingsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像サービング公開設定を持つ会社へのハンドル。 |
| contextHandle | `xsd:string` | はい | 公開コンテキストを処理します。 |

**出力**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| publishSettingArray | `xsd:string` | はい | Image Server 公開設定の配列。 |
