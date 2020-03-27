---
description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは初期設定のカタログに添付できます。
seo-description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは初期設定のカタログに添付できます。
seo-title: コマンドマクロ
solution: Experience Manager
title: コマンドマクロ
topic: Scene7 Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは初期設定のカタログに添付できます。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名</span></span> </p> </td> 
  <td class="stentry"> <p>マクロ名。 </p></td> 
 </tr> 
</table>

` *`nameは`*` 、大文字と小文字が区別されず、ASCII文字、数字、「 — 」、「_」、「。」の任意の組み合わせで構成される場合があります。 文字.

マクロは、リクエスト内で&#39;?&#39;の後の任意の場所、およびフィールド内の任意の場所で呼び出すこ `catalog::Modifier` とがで `catalog::PostModifier` きます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表し、「&amp;」区切り文字を使用して他のコマンドと区切る必要があります。

マクロ呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求内のマクロの呼び出しの前に発生した場合、要求内の同じコマンドより優先されます。 これは、要求文字列内 `catalog::Modifier`のコマンドが、要求内の位置に関係なく、文字列内のコ `catalog::Modifier` マンドを常に上書きする場合とは異なります。

コマンドマクロは引数の値を持つことはできませんが、カスタム変数を使用して要求の値をマクロに渡すことができます。

マクロは、次の制限を持つネスト可能です。マクロを呼び出すには、マクロ定義が解析時に既に定義されている場合、同じマクロ定義ファイル内で前に表示されている場合、またはデフォルトのマクロ定義ファイルに埋め込まれたマクロの定義を配置する必要があります。

## 例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

同じ属性を異なる画像に適用する場合、マクロが役立ちます。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

共通属性のマクロを定義できます。

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

マクロは次のように使用されます。

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

3番目 `wid=` の要求は異なるので、マクロが呼び出された後で値を上書きします *(前に指定しても*`wid=`**`$view$`、何も起こりません)。

## 関連項目 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) 、 [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)、マクロ [定義リファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
