---
title: コマンド マクロ
description: コマンド マクロは、コマンドのセットに名前付きショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、イメージ カタログまたは既定のカタログにアタッチできます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# コマンド マクロ{#command-macros}

コマンド マクロは、コマンドのセットに名前付きショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、イメージ カタログまたは既定のカタログにアタッチできます。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> の名前 </span></span> </p> </td> 
  <td class="stentry"> <p>マクロ名。 </p></td> 
 </tr> 
</table>

`*`name`*` では大文字と小文字が区別されません。また、ASCII 文字、数字、「–」、「_」、「。」を任意に組み合わせて使用できます 文字。

マクロは、リクエスト内の「?」より後の任意の場所、および `catalog::Modifier` または `catalog::PostModifier` フィールド内の任意の場所で呼び出すことができます。 マクロは、1 つ以上の完全な画像サービングコマンドのみを表すことができ、他のコマンドとは `&` の区切り文字で区切る必要があります。

マクロ呼び出しは、解析中に置換文字列に置き換えられます。 マクロ内のコマンドは、リクエスト内のマクロ呼び出しの前に発生した場合、リクエスト内の同じコマンドを上書きします。 この処理フローは `catalog::Modifier` とは異なります。リクエスト内の位置に関係なく、リクエスト文字列内のコマンドは常にリク `catalog::Modifier` スト文字列内のコマンドを上書きします。

コマンド マクロに引数値を指定することはできませんが、カスタム変数を使用して要求からマクロに値を渡すことができます。

マクロはネストできます。 ただし、マクロ定義の解析時に既に定義されている場合にのみ、マクロを呼び出すことができます。 このワークフローは、同じマクロ定義ファイルの前に表示するか、埋め込まれたマクロの定義を既定のマクロ定義ファイルに配置することで実行されます。

## 例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

マクロは、同じ属性を異なる画像に適用する場合に役立ちます。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

共通の属性用のマクロを定義できます。

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

マクロは次のように使用されます。

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

3 回目のリクエストでは `wid=` が異なるので、マクロが呼び出された *after* の値を上書きするだけです（「before `wid=`**`$view$` を指定しても効果はありません）。

## 関連項目 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2)、[catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)、[ マクロ定義リファレンス ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
