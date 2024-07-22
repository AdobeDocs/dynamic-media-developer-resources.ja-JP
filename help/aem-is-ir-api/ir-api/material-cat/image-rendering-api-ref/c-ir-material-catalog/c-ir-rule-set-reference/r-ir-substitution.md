---
title: 受継
description: 置換文字列要素。 <rule> 要素内ではオプションです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# 受継{#substitution}

置換文字列要素。 `<rule>` 要素ではオプションです。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

なし

## データ {#section-a2688866ed6d41279a8478886e511ae3}

置換文字列。

## 説明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

パスまたはクエリで一致した文字列または部分文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切られた）が含まれている場合、最初に一致したサブ文字列は置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合、一致した文字列全体が置換されます。

`<expression>` が空または存在しない場合は、置換文字列がパスまたはクエリに追加されます。

`<substitution>` が空の場合、一致した文字列または部分文字列は削除されます。 `<substitution>` を指定しない場合、パスまたはクエリ文字列は変更されません。

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

置換文字列にリテラル &lt; および&amp;文字を含めることはできません。 これらの予約文字は、それぞれ `&` および `<` でエンコードすることができます。または、文字列全体を XML `CDATA` セクションで囲むことができます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
