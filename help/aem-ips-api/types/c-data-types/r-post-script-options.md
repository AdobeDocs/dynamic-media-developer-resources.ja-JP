---
description: PostScript ファイルオプション。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 13%

---

# PostScriptOptions{#postscriptoptions}

PostScript ファイルオプション。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| プロセス | `xsd:string` | PostScript プロセスの選択。 |
| resolution | `xsd:double` | ファイルの解像度。 |
| カラースペース | `xsd:string` | PostScript カラースペースモード。 |
| 英 | `xsd:boolean` | ファイルを画像にラスタライズするかどうか。 その場合、元のファイルがこの方法で定義されている場合は、透明な背景が作成されます。 一般に、オーバーレイロゴの作成に使用されます。 |
| extractSearchWords | `xsd:boolean` | PostScript ファイルから検索語を抽出するかどうか。 |
