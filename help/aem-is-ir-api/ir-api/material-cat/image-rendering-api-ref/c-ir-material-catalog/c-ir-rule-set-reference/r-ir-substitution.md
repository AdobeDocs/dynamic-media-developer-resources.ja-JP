---
description: 置換文字列要素。 <rule>要素のオプションです。
seo-description: 置換文字列要素。 <rule>要素のオプションです。
seo-title: 置換
solution: Experience Manager
title: 置換
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 置換{#substitution}

置換文字列要素。 要素のオプシ `<rule>` ョンです。

## Attributes {#section-d955eefc53eb4274861270669c01f9ca}

なし

## データ {#section-a2688866ed6d41279a8478886e511ae3}

置換文字列。

## 説明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

パスまたはクエリ内で一致した文字列またはサブ文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切る）が含まれる場合、一致した最初のサブ文字列が置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合は、一致した文字列全体が置換されます。

が空の `<expression>` 場合や存在しない場合は、置換文字列がパスまたはクエリに追加されます。

が空の `<substitution>` 場合、一致した文字列またはサブ文字列が削除されます。 を指 `<substitution>` 定しない場合、パスまたはクエリ文字列は変更されません。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

置換文字列には、リテラル&lt;と&amp;文字を含めることはできません。 これらの予約文字は、それぞ `&` れとでエ `<`ンコードするか、文字列全体をXMLセクションで囲むことがで `CDATA` きます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
