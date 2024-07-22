---
description: 正規表現のパターン要素。 <rule> 要素内ではオプションです。
solution: Experience Manager
title: 式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# 式{#expression}

正規表現のパターン要素。 `<rule>` 要素ではオプションです。

## 属性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

なし

## データ {#section-e2601008d71243109af1a8c55b58416d}

正規表現のパターン文字列。

## 説明 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>` 要素は空にすることも、単純な検索文字列や正規表現パターンを含めることもできます。 パターンは、リクエスト文字列全体に適用されます。

`<expression>` が空の場合や指定されていない場合は、常に一致が発生します。これは、`<expression>.*</expression>` を指定することと同じです。

実装は、Perl に似た正規表現構文を提供する Java パッケージ [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) に基づいています。

## 説明 {#section-10b472a902674893b49ca49a7052c366}

式の文字列にリテラル &lt; および&amp;文字を含めることはできません。 これらの予約文字は、それぞれ `&` および `<` でエンコードすることができます。または、文字列全体を XML `CDATA` セクションで囲むことができます。

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>` タグと `</expression>` タグの間にあるすべての文字（オプションの `CDATA` セクション外の文字を含む）は、正規表現パーサーに渡されます。 余分な空白を避けるために注意する必要があります。

## 関連項目 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
