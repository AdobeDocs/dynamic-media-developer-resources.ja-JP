---
description: 正規表現パターン要素。 <rule>要素のオプションです。
seo-description: 正規表現パターン要素。 <rule>要素のオプションです。
seo-title: 式
solution: Experience Manager
title: 式
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 式{#expression}

正規表現パターン要素。 要素のオプシ `<rule>` ョンです。

## Attributes {#section-fd0574eee1f9423cbb2ed709c0906800}

なし

## データ {#section-4cd740c511a1432da0955e9acfbcf96f}

正規表現パターン文字列。

## 説明 {#section-3245c8a531bb455d8398449f6ea63b37}

この要 `<expression>` 素は、空の場合も、単純な検索文字列または正規表現パターンを含む場合もあります。 パターンは、リクエスト文字列全体に適用されます。

が空の場合、または指定されてい `<expression>` ない場合は、常に一致が発生します。これは、を指定することと同じで `<expression>.*</expression>`す。

この実装はJavaパッケージ [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)（Perlの構文と同様の正規表現構文を提供）に基づいています。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

式の文字列には、リテラル&lt;と&amp;を含めることはできません。 これらの予約文字は、それぞ `&` れとでエ `<`ンコードするか、文字列全体をXMLセクションで囲むことがで `CDATA` きます。

`<expression><![CDATA[&fmt=custom]]></expression>`

タグとタグの間のすべ `<expression>` ての文 `</expression>` 字（オプションセクションの外の文字を含む）が正規表現パーサーに渡さ `CDATA` れます。 余分な空白を避けるために注意が必要です。

## 関連項目 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
