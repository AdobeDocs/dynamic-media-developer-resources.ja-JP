---
title: ロケール
description: 翻訳ロケール Id。 要求のロケール ID を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# ロケール{#locale}

翻訳ロケール Id。 要求のロケール ID を指定します。

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ロケール ID （文字列）。 </p></td> 
 </tr> 
</table>

この ID と、で指定されたルールの使用 `attribute::LocaleMap` および `attribute::LocaleStrMap`、画像サービングは、オプションのカタログ ID 翻訳と文字列のローカライゼーションを適用します。

## プロパティ {#section-1854a9902b884d9b8e8e713b6635723f}

リクエストコマンド。 指定された場所に関係なく、ネストされたリクエストや埋め込みリクエストを含む、リクエスト全体に適用されます。 `locId` には、印刷可能な ASCII 文字のみを含める必要があります。 この要求のメインカタログにローカリゼーションマップが定義されていない場合は無視されます。 空または無効の場合はエラーが返されます `locId` が指定され、にデフォルトのルールが定義されていません `attribute::DefaultLocale`.

## 初期設定 {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` は、locale=が指定されていない場合に使用されます。

## 関連項目 {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)，ローカリゼーションサポート
