---
description: リクエストタイプ。 リクエストのタイプを指定します。
solution: Experience Manager
title: 要
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# 要{#req}

リクエストタイプ。 リクエストのタイプを指定します。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`options`*]`

* [catalogprops](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [画像セット](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [マップ](r-map-req.md)
* [マスク](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [prop](r-props.md)
* [解決](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [セット](r-set.md)
* [ターゲット](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [検証](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

詳細な説明に特に記載がない限り、サーバーは MIME タイプ `text` の応答 `text/plain` 返します。 多くのリクエストタイプでは、応答のタイプ（通常は default、`text`、`javascript`、`xml` である `json` など）を指定できます。 関連付けられている応答の MIME タイプは、それぞれ `text/plain`、`text/javascript`、`text/xml`、`text/javascript` です。

特に指定がない限り、応答は応答を `name=value` ペアのセットとしてフォーマットします。

[&#x200B; プロパティ &#x200B;](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) を参照してください。
