---
title: コマンドマクロ
description: コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは既定のカタログにアタッチできます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは既定のカタログにアタッチできます。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名前</span></span> </p> </td> 
  <td class="stentry"> <p>マクロ名。 </p></td> 
 </tr> 
</table>

`*`名前`*` は大文字と小文字を区別せず、ASCII 文字、数字、「 — 」、「_」、「。」の組み合わせで構成することもできます。 文字.

マクロは、リクエスト内の「?」より後の任意の場所、および `catalog::Modifier` または `catalog::PostModifier` フィールドに入力します。 マクロは、1 つ以上の、完全な、画像サービングコマンドのみを表し、を使用して他のコマンドと区切る必要があります。 `&` 区切り文字

マクロの呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求でマクロが呼び出される前に発生した場合、要求内の同じコマンドを上書きします。 この処理フローは、 `catalog::Modifier`( リクエスト文字列のコマンドは常に `catalog::Modifier` 文字列内の位置に関係なく、

コマンドマクロに引数値を含めることはできませんが、カスタム変数を使用してリクエストの値をマクロに渡すことができます。

マクロはネストできます。 ただし、マクロは、マクロ定義が解析された時点で既に定義されている場合にのみ呼び出すことができます。 このワークフローは、同じマクロ定義ファイル内で前に表示されるか、埋め込みマクロの定義を既定のマクロ定義ファイル内に配置することで実行されます。

## 例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

マクロは、異なる画像に同じ属性を適用する場合に役立ちます。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

次の共通属性のマクロを定義できます。

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

このマクロは次のように使用されます。

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

理由： `wid=` が 3 番目のリクエストと異なる場合は、 *次より後* マクロが呼び出されます ( `wid=`*前* `$view$` には何の効果もありません )。

## 関連項目 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [マクロ定義の参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
