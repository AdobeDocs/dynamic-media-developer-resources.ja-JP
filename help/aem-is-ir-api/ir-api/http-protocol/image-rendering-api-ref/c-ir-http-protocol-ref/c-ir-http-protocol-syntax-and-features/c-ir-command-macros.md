---
description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。
seo-description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。
seo-title: コマンドマクロ*
solution: Experience Manager
title: コマンドマクロ*
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 1%

---


# コマンドマクロ*{#command-macros}

コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。

`$ *[!DNL name]*$`

** *[!DNL name]* **マクロ名

マクロは、個別のマクロ定義ファイルで定義され、マテリアルカタログや既定のカタログにアタッチできます。

*[!DNL name]* では大文字と小文字が区別されません。また、ASCII文字、数字、「 — 」、「_」、「。」の組み合わせで構成することができます。文字.

リクエスト内で&#39;?&#39;の後、または`vignette::Modifier`フィールド内の任意の場所でマクロを呼び出します。 マクロは、1つ以上の完全な画像レンダリングコマンドのみを表すことができ、他のコマンドとは「&amp;」区切り文字で区切る必要があります。

マクロ呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求でマクロを呼び出す前に発生した場合、要求内の同じコマンドよりも優先されます。 これは、`vignette::Modifier`とは異なります。要求文字列内のコマンドは、要求内の位置に関係なく、`vignette::Modifier`文字列内のコマンドを常に上書きします。

コマンドマクロには引数の値を指定できませんが、カスタム変数を使用して要求の値をマクロに渡すことができます。

マクロは入れ子にできません。

**例**

マクロは、同じコマンドや属性を異なるレンダリングイメージに適用する場合に便利です。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

次の共通属性に対してマクロを定義できます。

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

このマクロは次のように使用されます。

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

`qlt=`は3番目の要求とは異なるので、マクロの呼び出し後に値を上書きします（`qlt=`*before* `$render$`を指定しても何も起こりません）。

**関連項目**

`catalog::MacroFile`,  `catalog::Modifier`，マクロ定義リファレンス

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

