---
description: 置換文字列要素。 <rule>要素のオプションです。
solution: Experience Manager
title: 置換
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# 置換{#substitution}

置換文字列要素。 `<rule>`要素のオプションです。

## 属性{#section-d955eefc53eb4274861270669c01f9ca}

なし

## データ {#section-a2688866ed6d41279a8478886e511ae3}

置換文字列。

## 説明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

パスまたはクエリ内で、一致した文字列またはサブ文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切る）が含まれる場合、一致した最初のサブ文字列が置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合は、一致した文字列全体が置換されます。

`<expression>`が空の場合や存在しない場合は、置換文字列がパスまたはクエリに追加されます。

`<substitution>`が空の場合、一致した文字列またはサブ文字列は削除されます。 `<substitution>`を指定しない場合、パスまたはクエリ文字列は変更されません。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

置換文字列には、リテラル&lt;と&amp;文字を含めることはできません。 これらの予約文字は、それぞれ`&`と`<`でエンコードできます。また、文字列全体をXML `CDATA`セクションに含めることもできます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
