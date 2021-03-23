---
description: カラープロファイルを埋め込む 作業中のICCカラープロファイルまたはicc=で指定されたプロファイルを、返信画像に埋め込むかどうかを指定します。
seo-description: カラープロファイルを埋め込む 作業中のICCカラープロファイルまたはicc=で指定されたプロファイルを、返信画像に埋め込むかどうかを指定します。
seo-title: iccEmbed
solution: Experience Manager
title: iccEmbed
uuid: ccd3fd2f-6f73-4725-a51a-9daf643d71af
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# iccEmbed{#iccembed}

カラープロファイルを埋め込む 作業中のICCカラープロファイルまたはicc=で指定されたプロファイルを、返信画像に埋め込むかどうかを指定します。

`iccEmbed=0|1`

## プロパティ {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

要求属性。 埋め込み可能なプロファイルがない場合は無視されます。

## 初期設定 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`を使用します。出力画像にICCプロファイルを埋め込むことはできません。出力画像形式でICCプロファイルの埋め込みがサポートされていない場合は無視されます。

詳しくは、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)を参照してください。

## 関連項目 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
