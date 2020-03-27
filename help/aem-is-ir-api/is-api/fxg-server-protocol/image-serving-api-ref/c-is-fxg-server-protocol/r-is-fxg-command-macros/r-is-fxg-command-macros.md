---
description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。
seo-description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。
seo-title: コマンドマクロ
solution: Experience Manager
title: コマンドマクロ
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b

---


# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。

マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは初期設定のカタログに添付できます。

マクロは、リクエスト内で&#39;?&#39;の後の任意の場所、およびフィールド内の任意の場所で呼び出すことがで `catalog::Modifier` きます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表すので、区切り文字「&amp;」で囲む必要があります（修飾子文字列の先頭または末尾を除く）。

マクロ呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求内のマクロの呼び出しの前に発生した場合、要求内の同じコマンドより優先されます。 これは、要求文字列内 `catalog::Modifier`のコマンドが、要求内の位置に関係なく、文字列内のコ `catalog::Modifier` マンドを常に上書きする場合とは異なります。

マクロは、次の制限を持つネスト可能です。マクロを呼び出すには、マクロ定義が解析時に既に定義されている場合、同じマクロ定義ファイルで前に表示されている場合、またはデフォルトのマクロ定義ファイルに埋め込まれたマクロの定義を配置する必要があります。

同じ属性を異なる画像に適用する場合、マクロが役立ちます。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

共通属性のマクロを定義できます。

`view wid=240&fmt=pdf&imageRes=300`

マクロは次のように使用されます。

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

3番目 `wid=` の要求は異なるので、マクロが呼び出された後で値を上書きします *(前に指定しても*`wid=`**`$view$`、何も起こりません)。

+ [name](r-name.md)
