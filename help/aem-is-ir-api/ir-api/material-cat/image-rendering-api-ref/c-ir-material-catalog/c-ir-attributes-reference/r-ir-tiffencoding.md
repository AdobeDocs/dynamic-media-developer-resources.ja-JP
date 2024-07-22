---
title: TiffEncoding
description: TIFFのエンコード形式。 TIFFイメージの圧縮形式を指定します（fmt= コマンドの 3 番目の値のデフォルトです）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# TiffEncoding{#tiffencoding}

TIFFのエンコード形式。 TIFFイメージの圧縮形式を指定します（`fmt=` コマンドの 3 番目の値のデフォルト）。

圧縮しない場合は `0`、LZW の場合は `1`、deflate （ZIP）の場合は `2`、JPEG圧縮の場合は `3` に設定します。

## プロパティ {#section-469f5a1225464542866f5353edd92db3}

列挙値。

## 初期設定 {#section-a3c5152a9f464e4987ed7c05d35b1169}

定義されていない場合または空の場合は `default::TiffEncoding` から継承します。

## 関連項目 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
