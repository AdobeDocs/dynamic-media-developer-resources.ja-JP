---
title: iccEmbed
description: カラープロファイルを埋め込みます。 作業中の ICC カラープロファイルまたは icc=で指定されたプロファイルを返信画像に埋め込むかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# iccEmbed{#iccembed}

カラープロファイルを埋め込みます。 作業中の ICC カラープロファイルまたは icc=で指定されたプロファイルを返信画像に埋め込むかどうかを指定します。

`iccEmbed=0|1`

## プロパティ {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

リクエスト属性。 埋め込みに使用できるプロファイルがない場合は無視されます。

## 初期設定 {#section-01948f6cd7a2415091004cd7526436c7}

出力画像に ICC プロファイルを埋め込まない `iccEmbed=0` 合。 出力画像形式が ICC プロファイルの埋め込みをサポートしていない場合は無視されます。

詳しくは、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) を参照してください。

## 関連項目 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) , [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
