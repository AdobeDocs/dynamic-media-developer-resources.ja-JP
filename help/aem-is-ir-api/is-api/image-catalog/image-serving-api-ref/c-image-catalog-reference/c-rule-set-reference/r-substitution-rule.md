---
description: 置換文字列要素。 <rule> 要素内ではオプションです。
solution: Experience Manager
title: 受継
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# 受継{#substitution}

置換文字列要素。 `<rule>` 要素ではオプションです。

## 属性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

なし

## データ {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

置換文字列。

## 説明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

パスまたはクエリで一致した文字列または部分文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切られた）が含まれている場合、最初に一致したサブ文字列は置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合、一致した文字列全体が置換されます。

`<expression>` が空または存在しない場合は、置換文字列がパスまたはクエリに追加されます。

`<substitution>` が空の場合、一致した文字列または部分文字列は削除されます。 `<substitution>` を指定しない場合、パスまたはクエリ文字列は変更されません。

>[!NOTE]
>
>この `<substitution>` 要素が属する `<rule>`,element に `replace="all"` が指定されている場合、入力文字列内のすべての一致が置換されます。 デフォルトでは、最初の一致のみが置換文字列に置き換えられます。

## Note {#section-cedf2adabaaf441c9f598fb0ea180246}

置換文字列にリテラル &lt; および&amp;文字を含めることはできません。 これらの予約文字は、それぞれ `&` および `<` でエンコードすることができます。または、文字列全体を XML CDATA セクションに含めることができます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
