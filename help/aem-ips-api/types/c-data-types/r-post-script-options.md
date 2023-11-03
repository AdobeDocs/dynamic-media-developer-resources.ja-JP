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
| colorspace | `xsd:string` | PostScript カラースペースモード。 |
| 英 | `xsd:boolean` | ファイルを画像にラスタライズするかどうか。 その場合、元のファイルがこの方法で定義されている場合は、透明な背景が作成されます。 一般に、オーバーレイロゴの作成に使用されます。 |
| extractSearchWords | `xsd:boolean` | PostScript ファイルから検索語を抽出するかどうか。 |
