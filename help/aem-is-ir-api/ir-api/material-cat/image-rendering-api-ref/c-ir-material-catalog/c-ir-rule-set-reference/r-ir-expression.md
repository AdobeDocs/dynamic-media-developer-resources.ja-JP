---
description: 正規表現パターン要素。 <rule> 要素内ではオプションです。
solution: Experience Manager
title: 式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 3%

---

# 式{#expression}

正規表現パターン要素。 `<rule>` 要素ではオプションです。

## 属性 {#section-fd0574eee1f9423cbb2ed709c0906800}

なし

## データ {#section-4cd740c511a1432da0955e9acfbcf96f}

正規表現のパターン文字列。

## 説明 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>` 要素は空にすることも、単純な検索文字列や正規表現パターンを含めることもできます。 パターンは、リクエスト文字列全体に適用されます。

`<expression>` が空の場合や指定されていない場合は、常に一致が発生します。これは、`<expression>.*</expression>` を指定することと同じです。

この実装は、Perl に似た正規表現構文を提供する Java パッケージ [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e) に基づいています。

## Note {#section-6b41a900b0ce4a9590e5861e3c81599c}

式の文字列にリテラル &lt; および&amp;文字を含めることはできません。 これらの予約文字は、それぞれ `&` および `<` でエンコードすることができます。または、文字列全体を XML `CDATA` セクションで囲むことができます。

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>` タグと `</expression>` タグの間にあるすべての文字（オプションの `CDATA` セクション外の文字を含む）は、正規表現パーサーに渡されます。 余分な空白を避けるために注意する必要があります。

## 関連項目 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
