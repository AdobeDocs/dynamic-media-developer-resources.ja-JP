---
description: 置換文字列要素。 <rule>要素のオプションです。
solution: Experience Manager
title: 置換
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# 置換{#substitution}

置換文字列要素。 `<rule>`要素ではオプションです。

## 属性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

なし

## データ {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

置換文字列。

## 説明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

パスまたはクエリ内の一致した文字列または部分文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切られた）が含まれる場合、一致した最初のサブ文字列が置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合は、一致した文字列全体が置き換えられます。

`<expression>`が空の場合や存在しない場合は、代替文字列がパスまたはクエリに追加されます。

`<substitution>`が空の場合、一致する文字列または部分文字列が削除されます。 `<substitution>`を指定しない場合、パスまたはクエリ文字列は変更されません。

>[!NOTE]
>
>`<rule>`で`replace="all"`が指定されている場合、入力文字列内の一致がすべて置き換えられ、`<substitution>`要素が属する要素に置き換えられます。 デフォルトでは、最初の一致のみが置換文字列に置き換えられます。

## Note {#section-cedf2adabaaf441c9f598fb0ea180246}

置換文字列にリテラル&lt;と&amp;文字を含めることはできません。 これらの予約文字は、それぞれ`&`と`<`でエンコードできます。また、文字列全体をXML CDATAセクションで囲むこともできます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
