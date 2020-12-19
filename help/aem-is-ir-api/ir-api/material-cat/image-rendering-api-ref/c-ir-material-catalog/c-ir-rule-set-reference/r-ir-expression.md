---
description: 正規式パターン要素。 <rule>要素のオプションです。
seo-description: 正規式パターン要素。 <rule>要素のオプションです。
seo-title: 式
solution: Experience Manager
title: 式
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# 式{#expression}

正規式パターン要素。 `<rule>`要素のオプションです。

## 属性{#section-fd0574eee1f9423cbb2ed709c0906800}

なし

## データ {#section-4cd740c511a1432da0955e9acfbcf96f}

正規式パターン文字列。

## 説明 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>`要素は、空にすることも、単純な検索文字列や正規式パターンを含めることもできます。 このパターンは、リクエスト文字列全体に適用されます。

`<expression>`が空の場合、または指定されていない場合、常に一致が発生します。これは、`<expression>.*</expression>`を指定することと同じです。

この実装はJavaパッケージ[java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)に基づいており、Perlと同様の正規式構文を提供しています。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

式文字列には、リテラルの&lt;および&amp;文字を含めることはできません。 これらの予約文字は、それぞれ`&`と`<`でエンコードできます。また、文字列全体をXML `CDATA`セクションに含めることもできます。

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`タグと`</expression>`タグの間のすべての文字は、オプションの`CDATA`セクション外の文字を含め、正規式パーサーに渡されます。 余分な空白がないように注意する必要があります。

## 関連項目 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
