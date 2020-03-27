---
description: 相対画像URLのルートURL。 相対画像URLのルートURLを指定します。 属性src=値が{波括弧}で囲まれている場合、属性RootPathの代わりにattribute RootUrlが使用されます。
seo-description: 相対画像URLのルートURL。 相対画像URLのルートURLを指定します。 属性src=値が{波括弧}で囲まれている場合、属性RootPathの代わりにattribute RootUrlが使用されます。
seo-title: RootUrl *
solution: Experience Manager
title: RootUrl *
topic: Scene7 Image Serving - Image Rendering API
uuid: aa10f210-4765-4b0e-9ce1-812b00cd8cf5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RootUrl *{#rooturl}

相対画像URLのルートURL。 相対画像URLのルートURLを指定します。 src=値が{波括弧}で囲まれている場合、attribute::RootUrlがattribute::RootPathの代わりに使用されます。

## プロパティ {#section-69cd0f71ea614770a8778c745d23197a}

テキスト文字列値。 先頭のプロトコル識別子を含む、絶対URLのルートパス。 次のプロトコルがサポートされています。HTTP、HTTPS、FTP。

## 初期設定 {#section-7a81569728474725a70f3a2cc4d48e85}

定義されていな `default::RootUrl` い場合は、から継承。 定義済みで空の場合、相対URLはこのマテリアルカタログではサポートされません。

## 関連項目 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
