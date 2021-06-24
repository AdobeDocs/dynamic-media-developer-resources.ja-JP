---
description: 正規表現パターン要素。 <rule>要素のオプションです。
solution: Experience Manager
title: 式
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---

# 式{#expression}

正規表現パターン要素。 `<rule>`要素ではオプションです。

## 属性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

なし

## データ {#section-e2601008d71243109af1a8c55b58416d}

正規表現パターン文字列。

## 説明 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>`要素は、空にすることも、単純な検索文字列や正規表現パターンを含めることもできます。 パターンはリクエスト文字列全体に適用されます。

`<expression>`が空の場合や指定されていない場合は、常に一致が発生します。これは、`<expression>.*</expression>`を指定するのと同じです。

この実装は、Javaパッケージ[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)に基づいており、Perlのと同様の正規表現構文を提供します。

## 説明 {#section-10b472a902674893b49ca49a7052c366}

式の文字列には、リテラル&lt;および&amp;文字を含めることはできません。 これらの予約文字は、それぞれ`&`と`<`でエンコードできます。また、文字列全体をXML `CDATA`セクションで囲むこともできます。

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`タグと`</expression>`タグの間のすべての文字が、オプションの`CDATA`セクション外の文字を含む正規表現パーサーに渡されます。 空白が余分に含まれないように注意する必要があります。

## 関連項目 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
