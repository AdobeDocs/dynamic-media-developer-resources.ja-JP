---
description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。
seo-description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。
seo-title: コマンドマクロ*
solution: Experience Manager
title: コマンドマクロ*
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# コマンドマクロ*{#command-macros}

コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。

`$ *[!DNL name]*$`

** *[!DNL name]* **マクロ名

マクロは、マテリアルカタログまたは既定のカタログにアタッチできる、個別のマクロ定義ファイルで定義されます。

*[!DNL name]* は大文字と小文字が区別されず、ASCII文字、数字、「 — 」、「_」、「。」の任意の組み合わせで構成できます。 文字.

リクエスト内で&#39;?&#39;の後、またはフィールド内の任意の場所でマクロを呼び出 `vignette::Modifier` します。 マクロは、1つ以上の完全な画像レンダリングコマンドのみを表し、「&amp;」区切り文字を使用して他のコマンドと区切る必要があります。

マクロ呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求内のマクロの呼び出しの前に発生した場合、要求内の同じコマンドより優先されます。 これは、要求文字列内 `vignette::Modifier`のコマンドが、要求内の位置に関係なく、文字列内のコ `vignette::Modifier` マンドを常に上書きする場合とは異なります。

コマンドマクロは引数の値を持つことはできませんが、カスタム変数を使用して要求の値をマクロに渡すことができます。

マクロは入れ子にできません。

**例**

マクロは、同じコマンドや属性を異なるレンダリングイメージに適用する場合に便利です。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

共通属性のマクロを定義できます。

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

マクロは次のように使用されます。

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

3番目 `qlt=` の要求は異なるので、マクロの呼び出し後に値を上書きします(beforeを指定し `qlt=`*ても&#x200B;*`$render$`何も起こりません)。

**関連項目**

`catalog::MacroFile`, `catalog::Modifier`，マクロ定義の参照

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

