---
description: リクエストタイプ。 リクエストのタイプを指定します。
solution: Experience Manager
title: req
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 9%

---

# req{#req}

リクエストタイプ。 リクエストのタイプを指定します。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`オプション`*]`

* [catalogprops](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
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

詳細な説明に特に記載がない限り、サーバーはMIMEタイプ`text/plain`の`text`応答を返します。 多くのリクエストタイプでは、`text`などの応答タイプを指定できます。通常は、`javascript`、`xml`、`json`です。 関連する応答のMIMEタイプは、それぞれ`text/plain`、`text/javascript`、`text/xml`、`text/javascript`です。

特に断りのない限り、応答は`name=value`のペアのセットとしてフォーマットされます。

[プロパティ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)を参照してください。
