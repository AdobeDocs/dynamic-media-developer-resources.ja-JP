---
description: PostScriptファイルオプション。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# PostScriptOptions{#postscriptoptions}

PostScriptファイルオプション。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`プロセス`*` | `xsd:string` | PostScriptプロセスの選択。 |
| `*`resolution`*` | `xsd:double` | ファイルの解像度。 |
| `*`カラースペース`*` | `xsd:string` | PostScriptカラースペースモード。 |
| `*`alpha`*` | `xsd:boolean` | ファイルを画像にラスタライズするかどうか。 がこの方法で定義されている場合、元のファイルがこの方法で定義されていると、透明な背景が作成されます。 一般に、オーバーレイロゴの作成に使用されます。 |
| `*`extractSearchWords`*` | `xsd:boolean` | PostScriptファイルから検索語を抽出するかどうか。 |
