---
description: PostScriptファイルのオプション。
seo-description: PostScriptファイルのオプション。
seo-title: PostScriptOptions
solution: Experience Manager
title: PostScriptOptions
topic: Scene7 Image Production System API
uuid: 31526bfe-b651-47a8-98c0-2750a3d9cabf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostScriptOptions{#postscriptoptions}

PostScriptファイルのオプション。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`プロセス`*` | `xsd:string` | PostScriptプロセスの選択 |
| ` *`解像度`*` | `xsd:double` | ファイルの解像度。 |
| ` *`カラースペース`*` | `xsd:string` | PostScriptカラースペースモード。 |
| ` *`alpha`*` | `xsd:boolean` | ファイルを画像にラスタライズするかどうか。 このように定義されている場合、元のファイルがこのように定義されていれば、透明な背景が作成されます。 一般に、重なり合うロゴの作成に使用されます。 |
| ` *`extractSearchWords`*` | `xsd:boolean` | PostScriptファイルから検索語を抽出するかどうか。 |

