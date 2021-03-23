---
description: 変換ロケールID 要求のロケールIDを指定します。
seo-description: 変換ロケールID 要求のロケールIDを指定します。
seo-title: ロケール
solution: Experience Manager
title: ロケール
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 5%

---


# locale{#locale}

変換ロケールID 要求のロケールIDを指定します。

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ロケールID（文字列） </p></td> 
 </tr> 
</table>

このIDと`attribute::LocaleMap`および`attribute::LocaleStrMap`で指定されたルールを使用して、画像サービングはオプションのカタログID変換と文字列ローカライゼーションを適用します。

## プロパティ {#section-1854a9902b884d9b8e8e713b6635723f}

リクエストコマンド 指定された場所に関係なく、ネストされた/埋め込まれたリクエストを含むリクエスト全体に適用されます。 `locId` には、印刷可能なASCII文字のみを含める必要があります。この要求のメインカタログでローカライゼーションマップが定義されていない場合は無視されます。 空または無効な`locId`が指定され、`attribute::DefaultLocale`にデフォルトのルールが定義されていない場合は、エラーが返されます。

## 初期設定 {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` は、locale=が指定されていない場合に使用されます。

## 関連項目 {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ,  [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),  [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e),ローカライゼーションサポート
