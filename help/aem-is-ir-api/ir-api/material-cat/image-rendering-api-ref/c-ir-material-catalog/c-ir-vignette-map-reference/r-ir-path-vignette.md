---
description: 周辺光量補正ファイルのパス ビネットファイルの相対パスと名前。
solution: Experience Manager
title: パス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5562b0e0-0476-4dd0-acce-058601b9af0a
TQID: 'https://experienceleague.adobe.com/70KfRxztxkghF-HS5uK-wPIelm-XGRF0ywyYnWxWNAw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 72
ht-degree: 9%

---

# パス{#path}

周辺光量補正ファイルのパス ビネットファイルの相対パスと名前。

サーバーは、この値と`attribute::RootPath`を組み合わせて、実際のビネット ファイル パスを構築します。 絶対パスにもできます。

## プロパティ {#section-b3b295feac084b56bd8a153c04987153}

テキスト文字列。 オプション。 指定する場合は、有効な相対または絶対ファイルパスである必要があります。 空の場合、`vignette::Modifier`には`vignette=` コマンドを含める必要があります。

## 初期設定 {#section-a1d2133856084eb79a5be8230a4b38fd}

なし

## 関連項目 {#section-177131dad5804964bfb8957c1f6e5191}

[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)、[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)

