---
description: パスデータを埋め込みます。 ビネットに埋め込まれたPhotoshopパスを応答画像に含めるかどうかを指定します。
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# pathEmbed{#pathembed}

パスデータを埋め込みます。 ビネットに埋め込まれたPhotoshopパスを応答画像に含めるかどうかを指定します。

`pathEmbed=0|1`

## プロパティ {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

要求属性。 ビネットにパスデータが含まれていない場合は無視されます。 パスデータは、必要に応じて`wid=`または`hei=`に縮小されます。

出力画像形式でパスの埋め込みがサポートされていない場合は無視されます。 パスの埋め込みをサポートする出力画像形式のリストについては、`fmt=`の説明を参照してください。

## 初期設定 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`を使用します。出力画像にパスを埋め込む必要はありません。

## 関連項目 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
