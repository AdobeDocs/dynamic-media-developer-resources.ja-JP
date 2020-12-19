---
description: リクエストのタイプ。 リクエストのタイプを指定します。
seo-description: リクエストのタイプ。 リクエストのタイプを指定します。
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 9%

---


# req{#req}

リクエストのタイプ。 リクエストのタイプを指定します。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`オプション`*]`

* [catalogprops](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [マップ](r-map-req.md)
* [mask](r-mask-req.md)
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

詳細な説明に特に記載がない限り、サーバはMIMEタイプ`text/plain`の`text`応答を返します。 多くのリクエストタイプでは、`text`などの応答タイプを指定できます。通常は、`javascript`、`xml`、`json`がデフォルトです。 関連する応答MIMEタイプは、それぞれ`text/plain`、`text/javascript`、`text/xml`、`text/javascript`です。

特に断りのない限り、応答は`name=value`のペアのセットとして形式設定されます。

「[プロパティ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)」を参照してください。
