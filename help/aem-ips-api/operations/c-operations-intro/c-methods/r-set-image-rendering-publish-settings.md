---
description: Scene7 開発者向け。 画像レンダリング材料カタログの参照 – カタログ属性セクションを参照してください。
solution: Experience Manager
title: setImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7b0fe5d2-2779-417f-a5fe-577def2e0158
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 13%

---

# setImageRenderingPublishSettings{#setimagerenderingpublishsettings}

Scene7 開発者向け。 画像レンダリング材料カタログの参照 – カタログ属性セクションを参照してください。

構文

## パラメーター {#section-d8980d38d4074312bf2bad65b0fed7f1}

**入力（setImageRenderingPublishSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社ハンドル。 |
| publishSettingsArray | `types:ConfigSettingArray` | はい | Scene7 開発者向け。 |
| contextHandle | `xsd:string` | いいえ | 公開コンテキストへのハンドル。 |
