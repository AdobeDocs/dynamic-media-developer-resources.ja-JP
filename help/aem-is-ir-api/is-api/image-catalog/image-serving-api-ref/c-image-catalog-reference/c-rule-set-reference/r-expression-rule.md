---
description: 正規式パターン要素。 <rule>要素のオプションです。
seo-description: 正規式パターン要素。 <rule>要素のオプションです。
seo-title: 式
solution: Experience Manager
title: 式
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---


# 式{#expression}

正規式パターン要素。 `<rule>`要素のオプションです。

## 属性{#section-2d438c889ae84b6da7e0ed84b5d021a0}

なし

## データ {#section-e2601008d71243109af1a8c55b58416d}

正規式パターン文字列。

## 説明 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>`要素は、空にすることも、単純な検索文字列や正規式パターンを含めることもできます。 このパターンは、リクエスト文字列全体に適用されます。

`<expression>`が空の場合、または指定されていない場合、常に一致が発生します。これは、`<expression>.*</expression>`を指定することと同じです。

この実装はJavaパッケージ[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)に基づいており、Perlと同様の正規式構文を提供しています。

## 説明 {#section-10b472a902674893b49ca49a7052c366}

式文字列には、リテラルの&lt;および&amp;文字を含めることはできません。 これらの予約文字は、それぞれ`&`と`<`でエンコードできます。また、文字列全体をXML `CDATA`セクションに含めることもできます。

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`タグと`</expression>`タグの間のすべての文字は、オプションの`CDATA`セクション外の文字を含め、正規式パーサーに渡されます。 余分な空白がないように注意する必要があります。

## 関連項目 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
