---
description: コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは既定のカタログに添付できます。
solution: Experience Manager
title: コマンドマクロ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。 マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは既定のカタログに添付できます。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>マクロ名。 </p></td> 
 </tr> 
</table>

`*``*` 名前では大文字と小文字が区別されません。また、ASCII文字、数字、「 — 」、「_」、「。」の組み合わせで構成することもできます。文字.

マクロは、リクエスト内で「?」より後の任意の場所、および`catalog::Modifier`フィールドまたは`catalog::PostModifier`フィールド内の任意の場所で呼び出すことができます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表し、他のコマンドとは「&amp;」区切り文字で区切る必要があります。

マクロの呼び出しは、解析の初期段階で置換文字列に置き換えられます。 マクロ内のコマンドは、リクエストでマクロを呼び出す前に発生した場合、リクエスト内の同じコマンドを上書きします。 これは`catalog::Modifier`とは異なります。要求文字列内のコマンドは、要求内の位置に関係なく、常に`catalog::Modifier`文字列内のコマンドを上書きします。

コマンドマクロに引数値は指定できませんが、カスタム変数を使用して要求の値をマクロに渡すことができます。

マクロはネストでき、次の制限があります。マクロは、マクロ定義が解析された時点で定義済みの場合にのみ呼び出すことができます。同じマクロ定義ファイル内に既に存在する場合や、その埋め込みマクロの定義を既定のマクロ定義ファイルに配置する場合です。

## 例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

マクロは、同じ属性を異なる画像に適用する場合に役立ちます。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

共通の属性に対してマクロを定義できます。

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

このマクロは次のように使用されます。

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

3番目のリクエストでは`wid=`が異なるので、マクロが呼び出された後の値&#x200B;**&#x200B;を上書きします（`wid=`*before* `$view$`を指定しても効果はありません）。

## 関連項目 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) 、 [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)、マクロ定義 [リファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
