---
description: PostScriptファイルのオプション。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
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

