---
title: 代用
description: 置換文字列要素。 <rule>要素ではオプションです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
TQID: 'https://experienceleague.adobe.com/GqJBLso7oigoeCJ-0KQzFv2aeoAiVzumjlDTtjBSDI4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 2%

---

# 代用{#substitution}

置換文字列要素。 `<rule>`要素ではオプションです。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

なし

## データ {#section-a2688866ed6d41279a8478886e511ae3}

置換文字列。

## 説明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

パスまたはクエリ内の一致した文字列または部分文字列の置換文字列を定義します。

パターン式に部分式（括弧で区切られた）が含まれる場合、最初に一致した部分文字列は置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合、一致した文字列全体が置換されます。

`<expression>`が空または存在しない場合、置換文字列がパスまたはクエリに追加されます。

`<substitution>`が空の場合、一致した文字列または部分文字列が削除されます。 `<substitution>`が指定されていない場合、パスまたはクエリ文字列は変更されません。

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

置換文字列にリテラルの&lt;および&amp;文字を含めることはできません。 これらの予約済み文字はそれぞれ`&`と`<`でエンコードできます。または、文字列全体をXML `CDATA` セクションで囲むことができます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`

