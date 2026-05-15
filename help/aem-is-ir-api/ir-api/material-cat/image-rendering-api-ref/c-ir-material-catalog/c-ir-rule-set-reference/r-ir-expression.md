---
description: 正規表現パターン要素。 <rule>要素ではオプションです。
solution: Experience Manager
title: 式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
TQID: 'https://experienceleague.adobe.com/zMAFfzeypXmMIx1aO1xmHdF-UkHJPHKp7KUgi05F94w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 3%

---

# 式{#expression}

正規表現パターン要素。 `<rule>`要素ではオプションです。

## 属性 {#section-fd0574eee1f9423cbb2ed709c0906800}

なし

## データ {#section-4cd740c511a1432da0955e9acfbcf96f}

正規表現パターン文字列。

## 説明 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>`要素は空にするか、単純な検索文字列または正規表現パターンを含めることができます。 パターンはリクエスト文字列全体に適用されます。

`<expression>`が空であるか指定されていない場合は、常に一致が発生します。これは、`<expression>.*</expression>`を指定することと同じです。

実装は、Java パッケージ [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)に基づいています。これは、Perlと同様の正規表現構文を提供します。

## Note {#section-6b41a900b0ce4a9590e5861e3c81599c}

式の文字列にリテラルの&lt;および&amp;文字を含めることはできません。 これらの予約済み文字はそれぞれ`&`と`<`でエンコードできます。または、文字列全体をXML `CDATA` セクションで囲むことができます。

`<expression><![CDATA[&fmt=custom]]></expression>`

タグ `<expression>`と`</expression>`の間のすべての文字が、オプションの`CDATA` セクション以外の文字を含む正規表現パーサーに渡されます。 余分な空白を避けるように注意する必要があります。

## 関連項目 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
