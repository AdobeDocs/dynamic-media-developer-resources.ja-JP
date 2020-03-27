---
description: 正規表現パターン要素。 <rule>要素のオプションです。
seo-description: 正規表現パターン要素。 <rule>要素のオプションです。
seo-title: 式
solution: Experience Manager
title: 式
topic: Scene7 Image Serving - Image Rendering API
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 式{#expression}

正規表現パターン要素。 要素のオプシ `<rule>` ョンです。

## Attributes {#section-2d438c889ae84b6da7e0ed84b5d021a0}

なし

## データ {#section-e2601008d71243109af1a8c55b58416d}

正規表現パターン文字列。

## 説明 {#section-759bfb738ddb45dba1f0807aba8c1113}

この要 `<expression>` 素は、空の場合も、単純な検索文字列または正規表現パターンを含む場合もあります。 パターンは、リクエスト文字列全体に適用されます。

が空の場合、または指定されてい `<expression>` ない場合は、常に一致が発生します。これは、を指定することと同じで `<expression>.*</expression>`す。

この実装はJavaパッケージ [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)（Perlの構文と同様の正規表現構文を提供）に基づいています。

## 説明 {#section-10b472a902674893b49ca49a7052c366}

式の文字列には、リテラル&lt;と&amp;を含めることはできません。 これらの予約文字は、それぞ `&` れとでエ `<`ンコードするか、文字列全体をXMLセクションで囲むことがで `CDATA` きます。

`<expression><![CDATA[&fmt=custom]]></expression>`

タグとタグの間のすべ `<expression>` ての文 `</expression>` 字（オプションセクションの外の文字を含む）が正規表現パーサーに渡さ `CDATA` れます。 余分な空白を避けるために注意が必要です。

## 関連項目 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
