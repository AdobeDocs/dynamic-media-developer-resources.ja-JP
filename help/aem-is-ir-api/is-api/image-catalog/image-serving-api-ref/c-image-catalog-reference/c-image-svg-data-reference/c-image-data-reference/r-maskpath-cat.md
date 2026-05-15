---
description: マスクファイルのパス このカタログレコードに関連付けられたマスク画像ファイルの相対パスまたは絶対パスと名前。
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
TQID: 'https://experienceleague.adobe.com/tUXD-vnkr3qkaH3B-dE-e9wfSPXAcnwRbqG9KuJej9E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 2%

---

# MaskPath{#maskpath}

マスクファイルのパス このカタログレコードに関連付けられたマスク画像ファイルの相対パスまたは絶対パスと名前。

画像に個別のマスクを添付できます。

サーバーは、[Source データの管理](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)で説明されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#section-cdc3b7e2811e41008479cd97887c01b7}

テキスト文字列値。 オプション。 指定する場合は、有効な相対または絶対のImage Server ファイルパスである必要があります。 ファイル サフィックスが存在しない場合、`attribute::DefaultExt`が追加されます。

メイン画像（`catalog::Path`）とマスク画像（`catalog::MaskPath`）の両方がカタログレコードで定義されている場合、両方とも同じピクセルサイズである必要があります。 マスク画像は8 ビットのグレースケールである必要があります。

リクエストの`mask=`が`catalog::MaskPath`を上書きします。

`catalog::MaskPath`は、メインイメージ （`catalog::Path`）内のアルファチャンネルをオーバーライドします。存在する場合は、アルファチャンネルが関連付けられていない場合（つまり、事前に乗算されていない場合）は、オーバーライドされます。 画像アルファが事前に乗算されている場合、`catalog::MaskPath`は無視され、アルファチャンネルは常に使用されます。

## 初期設定 {#section-78533e35bfec469ba087cb68a35bb81b}

なし

## 関連項目 {#section-68d262f5949c4959b8723ba44611d1dc}

[属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)、[属性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)、[ カタログ：:Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)、[ マスク=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)、[req=マスク ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
