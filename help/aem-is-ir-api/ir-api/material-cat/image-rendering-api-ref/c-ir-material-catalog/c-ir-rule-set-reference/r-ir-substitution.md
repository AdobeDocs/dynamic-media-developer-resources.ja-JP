---
description: 置換文字列要素。 <rule>要素のオプションです。
solution: Experience Manager
title: 置換
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# 置換{#substitution}

置換文字列要素。 `<rule>`要素ではオプションです。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

なし

## データ {#section-a2688866ed6d41279a8478886e511ae3}

置換文字列。

## 説明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

パスまたはクエリ内の一致した文字列またはサブ文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切られた）が含まれる場合、一致した最初のサブ文字列が置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合は、一致した文字列全体が置き換えられます。

`<expression>`が空の場合や存在しない場合は、代替文字列がパスまたはクエリに追加されます。

`<substitution>`が空の場合、一致する文字列またはサブ文字列が削除されます。 `<substitution>`を指定しない場合、パスまたはクエリ文字列は変更されません。

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

置換文字列にリテラル&lt;と&amp;文字を含めることはできません。 これらの予約文字は、それぞれ`&`と`<`でエンコードできます。また、文字列全体をXML `CDATA`セクションで囲むこともできます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
