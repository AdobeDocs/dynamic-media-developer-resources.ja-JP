---
title: IccDither
description: カラー変換ディザリング。 icc=で明示的な選択が行われない場合に、カラー変換の知覚的な品質を向上させるためにディザリングを使用する必要があるかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1bec31-3f7c-48c8-9456-6359b739a657
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 3%

---

# IccDither{#iccdither}

カラー変換ディザリング。 `icc=` で明示的な選択が行われない場合に、カラー変換の知覚的な品質を向上させるためにディザリングを使用するかどうかを指定します。

## プロパティ {#section-646fb48084734c66bf648360f3a5bfd1}

フラグ。 無効にするには `0` に設定し、ディザリングを有効にするには `1` に設定します。

## 初期設定 {#section-c9066c361215404d847f4d2c8f1ea3a5}

定義されていない場合または空の場合は `default::IccDither` から継承します。

## 関連項目 {#section-76a376a1bee74670867b4de81fea65aa}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
