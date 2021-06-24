---
description: カタログ識別子。 HTTP要求でビネット、マテリアル、またはICCプロファイルオブジェクト指定子でこのカタログを識別するために使用されるHTTPパス要素。
solution: Experience Manager
title: RootId
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: cc34087a-8a19-4ead-b510-f2466efc44a9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# RootId{#rootid}

カタログ識別子。 HTTP要求でビネット、マテリアル、またはICCプロファイルオブジェクト指定子でこのカタログを識別するために使用されるHTTPパス要素。

## プロパティ {#section-c33266223d5b47029df756caa4e0df0c}

テキスト文字列の値。 httpパスで有効な任意の文字を含めることができます。

## 初期設定 {#section-e0ed902557684345850b86672b5dbe5b}

なし. 各カタログには、一意の`catalog::RootId`値が必要です。 default.iniは通常空の`catalog::RootId`を持ちます。

## 関連項目 {#section-4670832574f54f9080bb485b047efd5b}

[catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85) 、 [vignette::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-id-vignette.md#reference-2a7ba758924b4757b3234942304db7fd)、 [profile::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-name.md#reference-63b663d2052545ffab030a23e7060b1e)、 [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
