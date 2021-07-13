---
description: コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。
solution: Experience Manager
title: コマンドマクロ*
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 1%

---

# コマンドマクロ*{#command-macros}

コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。

`$ *[!DNL name]*$`

** *[!DNL name]* **マクロ名

マクロは、別々のマクロ定義ファイルで定義され、マテリアルカタログまたは既定のカタログにアタッチできます。

*[!DNL name]* は大文字と小文字を区別せず、ASCII文字、数字、「 — 」、「_」、「。」の組み合わせで構成することもできます。文字.

リクエスト内の「?」の後の任意の場所、または`vignette::Modifier`フィールド内の任意の場所でマクロを呼び出します。 マクロは、1つ以上の完全な画像レンダリングコマンドのみを表し、他のコマンドとは「&amp;」区切り文字で区切る必要があります。

マクロの呼び出しは、解析の初期段階で置換文字列に置き換えられます。 マクロ内のコマンドは、リクエストでマクロを呼び出す前に発生した場合、リクエスト内の同じコマンドを上書きします。 これは`vignette::Modifier`とは異なります。要求文字列内のコマンドは、要求内の位置に関係なく、常に`vignette::Modifier`文字列内のコマンドを上書きします。

コマンドマクロに引数値は指定できませんが、カスタム変数を使用して要求の値をマクロに渡すことができます。

マクロはネストできない可能性があります。

**例**

マクロは、同じコマンドや属性を別のレンダリングイメージに適用する場合に役立ちます。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

共通の属性に対してマクロを定義できます。

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

このマクロは次のように使用されます。

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

3番目のリクエストでは`qlt=`が異なるので、マクロの呼び出し後に値を上書きします（`qlt=`*before* `$render$`は無効です）。

**関連項目**

`catalog::MacroFile`,  `catalog::Modifier`，マクロ定義のリファレンス

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
