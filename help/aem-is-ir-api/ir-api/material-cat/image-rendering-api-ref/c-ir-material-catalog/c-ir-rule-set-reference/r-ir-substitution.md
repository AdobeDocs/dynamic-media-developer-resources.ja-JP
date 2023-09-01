---
title: 置換
description: 置換文字列要素。 でのオプション <rule> 要素。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# 置換{#substitution}

置換文字列要素。 でのオプション `<rule>` 要素。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

なし

## データ {#section-a2688866ed6d41279a8478886e511ae3}

置換文字列。

## 説明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

パスまたはクエリ内の一致した文字列または部分文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切られた）が含まれる場合、最初に一致した部分文字列は置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合は、一致した文字列全体が置き換えられます。

次の場合 `<expression>` が空の場合や存在しない場合は、代替文字列がパスまたはクエリに追加されます。

次の場合 `<substitution>` が空の場合、一致した文字列または部分文字列が削除されます。 次の場合 `<substitution>` が指定されていない場合、パスまたはクエリー文字列は変更されません。

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

置換文字列にリテラル &lt; および&amp;文字を含めることはできません。 これらの予約文字は、 `&` および `<`、それぞれ、または文字列全体を XML で囲むことができます `CDATA` セクション：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
