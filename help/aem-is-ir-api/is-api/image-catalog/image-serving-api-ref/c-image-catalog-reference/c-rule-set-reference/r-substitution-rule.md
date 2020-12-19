---
description: 置換文字列要素。 <rule>要素のオプションです。
seo-description: 置換文字列要素。 <rule>要素のオプションです。
seo-title: 置換
solution: Experience Manager
title: 置換
topic: Scene7 Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# 置換{#substitution}

置換文字列要素。 `<rule>`要素のオプションです。

## 属性{#section-a4506fcb765f4f128f7f1f2629b18a6c}

なし

## データ {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

置換文字列。

## 説明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

パスまたはクエリー内で、一致した文字列またはサブ文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切る）が含まれる場合、一致した最初のサブ文字列が置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合は、一致した文字列全体が置換されます。

`<expression>`が空の場合や存在しない場合は、置換文字列がパスまたはクエリに追加されます。

`<substitution>`が空の場合、一致した文字列またはサブ文字列が削除されます。 `<substitution>`を指定しない場合、パスまたはクエリ文字列は変更されません。

>[!NOTE]
>
>`replace="all"`がこの`<substitution>`要素が属する`<rule>`,elementで指定されている場合、入力文字列内のすべての一致が置換されます。 デフォルトでは、最初に一致したものだけが置換文字列に置き換えられます。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

置換文字列には、リテラル&lt;と&amp;文字を含めることはできません。 これらの予約文字は、それぞれ`&`と`<`でエンコードできます。また、文字列全体をXML CDATAセクションに含めることもできます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
