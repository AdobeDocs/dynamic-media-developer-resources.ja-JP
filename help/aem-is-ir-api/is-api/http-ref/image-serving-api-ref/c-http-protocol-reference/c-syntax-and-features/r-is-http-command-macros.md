---
title: コマンドマクロ
description: コマンドマクロは、一連のコマンドに名前付きショートカットを提供します。 マクロは個別のマクロ定義ファイルで定義され、画像カタログまたはデフォルトカタログに添付できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
TQID: 'https://experienceleague.adobe.com/a7vbT8heEkiWfmxn3wPudnzYTRN-H-I5D22038P4mJE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 311
ht-degree: 0%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、一連のコマンドに名前付きショートカットを提供します。 マクロは個別のマクロ定義ファイルで定義され、画像カタログまたはデフォルトカタログに添付できます。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">名</span></span> </p> </td> 
  <td class="stentry"> <p>マクロ名。 </p></td> 
 </tr> 
</table>

`*`name`*`は大文字と小文字を区別せず、ASCII文字、数字、「 – 」、「_」、「。」の組み合わせで構成される可能性があります。

マクロは、「?」の後のリクエスト内の任意の場所、および`catalog::Modifier`または`catalog::PostModifier` フィールド内の任意の場所で呼び出すことができます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表します。また、`&`個の区切り記号を含む他のコマンドから区切る必要があります。

マクロ呼び出しは、パースの早い段階で代用文字列に置き換えられます。 マクロ内のコマンドは、リクエスト内のマクロ呼び出しの前に発生した場合、リクエスト内の同じコマンドを上書きします。 この処理フローは`catalog::Modifier`とは異なります。リクエスト文字列内のコマンドは、リクエスト内の位置に関係なく、`catalog::Modifier`文字列内のコマンドを常に上書きします。

コマンドマクロには引数の値を指定できませんが、カスタム変数を使用して、リクエストの値をマクロに渡すことができます。

マクロはネストできます。 ただし、マクロは、マクロ定義の解析時に既に定義されている場合にのみ呼び出すことができます。 このワークフローは、同じマクロ定義ファイル内で以前に表示するか、そのような埋め込みマクロの定義をデフォルトのマクロ定義ファイルに配置することによって実行されます。

## 例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

マクロは、同じ属性を異なる画像に適用する場合に便利です。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

共通の属性のマクロを定義できます。

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

マクロは次のように使用されます。

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

`wid=`は3番目のリクエストとは異なるため、マクロが呼び出された&#x200B;*後*&#x200B;の値を単純に上書きできます（`wid=`*前* `$view$`を指定しても効果はありません）。

## 関連項目 {#section-8cdba0ed2480444ca61e719e54f8871c}

[&#x200B; カタログ：:MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2)、[&#x200B; カタログ：:Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)、[&#x200B; マクロ定義参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
