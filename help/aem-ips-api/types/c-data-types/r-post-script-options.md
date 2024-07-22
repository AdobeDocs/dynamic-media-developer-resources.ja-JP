---
description: PostScript ファイルオプション。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 10%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript ファイルオプション。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| プロセス | `xsd:string` | PostScript プロセスの選択。 |
| resolution | `xsd:double` | ファイルの解像度。 |
| 色空間 | `xsd:string` | PostScript カラースペースモード。 |
| 英 | `xsd:boolean` | ファイルを画像にラスタライズするかどうか。 元のファイルがそのように定義されている場合、透明な背景が作成されます。 通常、オーバーレイするロゴの作成に使用します。 |
| extractSearchWords | `xsd:boolean` | 検索単語をPostScript ファイルから抽出するかどうか。 |
