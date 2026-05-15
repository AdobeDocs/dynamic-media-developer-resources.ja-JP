---
description: 置換文字列要素。 <rule>要素ではオプションです。
solution: Experience Manager
title: 代用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
TQID: 'https://experienceleague.adobe.com/ZdC23CxEXKYN0d-h7nM8588KTS5Vy6BTh0kl5Iseq0w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 1%

---

# 代用{#substitution}

置換文字列要素。 `<rule>`要素ではオプションです。

## 属性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

なし

## データ {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

置換文字列。

## 説明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

パスまたはクエリ内の一致した文字列または部分文字列の置換文字列を定義します。

パターン式にサブ式（括弧で区切られた）が含まれる場合、最初に一致した部分文字列は置換文字列に置き換えられます。 パターン式にサブ式が含まれていない場合、一致した文字列全体が置換されます。

`<expression>`が空または存在しない場合、置換文字列がパスまたはクエリに追加されます。

`<substitution>`が空の場合、一致した文字列または部分文字列が削除されます。 `<substitution>`が指定されていない場合、パスまたはクエリ文字列は変更されません。

>[!NOTE]
>
>この`<substitution>`要素が属する`<rule>`，要素で`replace="all"`が指定されている場合、入力文字列内のすべての一致が置換されます。 デフォルトでは、最初の一致のみが置換文字列に置き換えられます。

## Note {#section-cedf2adabaaf441c9f598fb0ea180246}

置換文字列にリテラルの&lt;および&amp;文字を含めることはできません。 これらの予約済み文字はそれぞれ`&`と`<`でエンコードするか、文字列全体をXML CDATA セクションで囲むことができます。

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
