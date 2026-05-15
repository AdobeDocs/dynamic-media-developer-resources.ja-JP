---
title: iccEmbed
description: カラープロファイルを埋め込みます。 作業中のICC カラープロファイルまたはicc=で指定されたプロファイルを返信画像に埋め込むかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
TQID: 'https://experienceleague.adobe.com/gIV48JpwNqevp2gw-E-tegSHco2R-f1IE3V1OLPPVvk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 3%

---

# iccEmbed{#iccembed}

カラープロファイルを埋め込みます。 作業中のICC カラープロファイルまたはicc=で指定されたプロファイルを返信画像に埋め込むかどうかを指定します。

`iccEmbed=0|1`

## プロパティ {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

リクエスト属性： 埋め込み可能なプロファイルがない場合は無視されます。

## 初期設定 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`。出力画像にICC プロファイルを埋め込むことはありません。 出力画像形式がICC プロファイルの埋め込みをサポートしていない場合は無視されます。

詳しくは、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)を参照してください。

## 関連項目 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[属性：:IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)、[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
