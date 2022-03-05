---
title: コマンドマクロ
description: コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。

`$ *[!DNL name]*$`

** *[!DNL name]* **マクロ名

マクロは、別のマクロ定義ファイルで定義され、マテリアルカタログまたは既定のカタログにアタッチできます。

*[!DNL name]* は大文字と小文字を区別せず、ASCII 文字、数字、「 — 」、「_」、「。」の組み合わせで構成することもできます。 文字.

リクエスト内の「?」の後の任意の場所、または `vignette::Modifier` フィールドに入力します。 マクロは、1 つ以上の画像レンダリングコマンドのみを表し、他のコマンドとは「&amp;」区切り文字で区切る必要があります。

マクロの呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求でマクロが呼び出される前に発生した場合、要求内の同じコマンドを上書きします。 このワークフローは、 `vignette::Modifier`( リクエスト文字列内のコマンドは、 `vignette::Modifier` 文字列を指定します。

コマンドマクロに引数値を含めることはできませんが、カスタム変数を使用してリクエストの値をマクロに渡すことができます。

マクロはネストできない可能性があります。

**例**

マクロは、同じコマンドや属性を別のレンダリングイメージに適用する場合に便利です。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

共通属性のマクロを定義できます。

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

このマクロは次のように使用されます。

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

理由： `qlt=` が 3 番目の要求と異なる場合は、マクロが呼び出された後に、ソフトウェアが値を上書きします ( `qlt=` *前* `$render$`無効です )。

**関連項目**

`catalog::MacroFile`, `catalog::Modifier`，マクロ定義リファレンス

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
