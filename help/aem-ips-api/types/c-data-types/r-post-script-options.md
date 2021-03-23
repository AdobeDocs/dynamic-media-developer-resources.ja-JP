---
description: PostScriptファイルのオプション。
seo-description: PostScriptファイルのオプション。
seo-title: PostScriptOptions
solution: Experience Manager
title: PostScriptOptions
uuid: 31526bfe-b651-47a8-98c0-2750a3d9cabf
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 10%

---


# PostScriptOptions{#postscriptoptions}

PostScriptファイルのオプション。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`プロセス`*` | `xsd:string` | PostScriptプロセスの選択 |
| `*`resolution`*` | `xsd:double` | ファイルの解像度。 |
| `*`カラースペース`*` | `xsd:string` | PostScriptカラースペースモード。 |
| `*`alpha`*` | `xsd:boolean` | ファイルを画像にラスタライズするかどうかを指定します。 このように定義されている場合、元のファイルがこのように定義されていれば、透明な背景が作成されます。 一般に、オーバーレイロゴの作成に使用されます。 |
| `*`extractSearchWords`*` | `xsd:boolean` | PostScriptファイルから検索語を抽出するかどうか。 |

