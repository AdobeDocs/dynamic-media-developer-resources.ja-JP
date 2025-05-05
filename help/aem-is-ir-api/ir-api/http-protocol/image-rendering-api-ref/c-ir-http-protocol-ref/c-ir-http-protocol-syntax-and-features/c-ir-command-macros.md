---
title: コマンド マクロ
description: コマンド マクロは、コマンドのセットに名前付きショートカットを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# コマンド マクロ{#command-macros}

コマンド マクロは、コマンドのセットに名前付きショートカットを提供します。

`$ *[!DNL name]*$`

**&#x200B; *[!DNL name]* &#x200B;** マクロ名

マクロは、個別のマクロ定義ファイルで定義され、マテリアル カタログまたは既定のカタログにアタッチできます。

*[!DNL name]* は、大文字と小文字が区別されず、ASCII 文字、数字、「–」、「_」、「。」の任意の組み合わせで構成できます。 文字。

&#39;?&#39;の後のリクエスト内の任意の場所、または `vignette::Modifier` フィールド内の任意の場所でマクロを呼び出します。 マクロは、1 つ以上の画像レンダリングコマンドのみを表すことができ、「&amp;」区切り記号を使用して他のコマンドと区切る必要があります。

マクロ呼び出しは、解析中に置換文字列に置き換えられます。 マクロ内のコマンドは、リクエスト内のマクロ呼び出しの前に発生した場合、リクエスト内の同じコマンドを上書きします。 このワークフローは `vignette::Modifier` とは異なります。リクエスト内の位置に関係なく、リクエスト文字列内のコマンドによって、リクエスト文字列内のコマンドによって `vignette::Modifier` の文字列のコマンドが上書きされます。

コマンド マクロに引数値を指定することはできませんが、カスタム変数を使用して要求からマクロに値を渡すことができます。

マクロはネストできません。

**例**

マクロは、同じコマンドまたは属性を別のレンダリング イメージに適用する場合に便利です。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

共通の属性用のマクロを定義できます。

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

マクロは次のように使用されます。

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

3 回目のリクエストでは `qlt=` が異なるので、マクロが呼び出された後に、ソフトウェアが値を上書きします（`qlt=`*before*`$render$` は無効）を指定します。

**関連トピック**

`catalog::MacroFile`, `catalog::Modifier`, マクロ定義リファレンス

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
