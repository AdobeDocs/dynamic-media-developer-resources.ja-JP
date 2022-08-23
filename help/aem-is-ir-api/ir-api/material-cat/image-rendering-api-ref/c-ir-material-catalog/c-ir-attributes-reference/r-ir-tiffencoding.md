---
title: TiffEncoding
description: TIFFのエンコーディング形式。 TIFF画像の圧縮形式を指定します（実際には、fmt=コマンドの 3 番目の値のデフォルトです）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 5%

---

# TiffEncoding{#tiffencoding}

TIFFのエンコーディング形式。 TIFF画像の圧縮形式を指定します ( 実際には、 `fmt=` コマンド ) を使用します。

に設定 `0` 圧縮しないので `1` LZW の場合 `2` deflate (ZIP) の場合、 `3` (JPEG圧縮 )

## プロパティ {#section-469f5a1225464542866f5353edd92db3}

列挙。

## 初期設定 {#section-a3c5152a9f464e4987ed7c05d35b1169}

継承元 `default::TiffEncoding` が定義されていない場合、または空の場合は。

## 関連項目 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
