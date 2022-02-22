---
title: pathEmbed
description: パスデータを埋め込みます。 ビネットに埋め込まれたPhotoshopパスを応答画像に含めるかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# pathEmbed{#pathembed}

パスデータを埋め込みます。 ビネットに埋め込まれたPhotoshopパスを応答画像に含めるかどうかを指定します。

`pathEmbed=0|1`

## プロパティ {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

要求属性。 ビネットにパスデータが含まれていない場合は無視されます。 パスデータは次の値に合わせて拡大縮小されます。 `wid=` および/または `hei=` 必要に応じて。

出力画像形式でパスの埋め込みがサポートされていない場合は無視されます。 詳しくは、 `fmt=` パスの埋め込みをサポートする出力画像形式のリスト。

## 初期設定 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`（出力画像にパスを埋め込まない場合）

## 関連項目 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
