---
description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義されます。マクロは、画像カタログまたは初期設定のカタログにアタッチできます。
seo-description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義されます。マクロは、画像カタログまたは初期設定のカタログにアタッチできます。
seo-title: コマンドマクロ
solution: Experience Manager
title: コマンドマクロ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---


# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義されます。マクロは、画像カタログまたは初期設定のカタログにアタッチできます。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>マクロ名。 </p></td> 
 </tr> 
</table>

`*``*` 名前は大文字と小文字が区別されず、ASCII文字、数字、「 — 」、「_」、「。」の任意の組み合わせで構成できます。文字.

マクロは、リクエストの中で&#39;?&#39;の後の任意の場所、および`catalog::Modifier`や`catalog::PostModifier`フィールド内の任意の場所で呼び出すことができます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表すことができ、他のコマンドとは「&amp;」区切り文字で区切る必要があります。

マクロ呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求でマクロを呼び出す前に発生した場合、要求内の同じコマンドよりも優先されます。 これは、`catalog::Modifier`とは異なります。要求文字列内のコマンドは、要求内の位置に関係なく、`catalog::Modifier`文字列内のコマンドを常に上書きします。

コマンドマクロには引数の値を指定できませんが、カスタム変数を使用して要求の値をマクロに渡すことができます。

マクロはネストできますが、次の制限があります。マクロは、同じマクロ定義ファイル内の前の位置に表示された場合、またはデフォルトのマクロ定義ファイルにその埋め込みマクロの定義を配置した場合にのみ、定義済みのマクロを呼び出すことができます。

## 例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

同じ属性を異なる画像に適用する場合、マクロが役立ちます。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

共通属性のマクロを定義できます。

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

このマクロは次のように使用されます。

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

`wid=`は3番目の要求とは異なるので、*の後の値*&#x200B;を上書きします（*`$view$`の前に`wid=`*&#x200B;を指定しても効果はありません）。

## 関連項目 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [マクロ定義リファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
