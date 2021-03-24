---
description: コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。
solution: Experience Manager
title: コマンドマクロ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットに名前付きのショートカットを提供します。

マクロは、個別のマクロ定義ファイルで定義されます。マクロは、画像カタログまたは初期設定のカタログにアタッチできます。

マクロは、リクエスト内で&#39;?&#39;の後の任意の場所、および`catalog::Modifier`フィールド内の任意の場所で呼び出すことができます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表すことができるので、区切り文字「&amp;」で囲む必要があります（修飾子文字列の先頭または末尾を除く）。

マクロ呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求でマクロを呼び出す前に発生した場合、要求内の同じコマンドよりも優先されます。 これは、`catalog::Modifier`とは異なります。要求文字列内のコマンドは、要求内の位置に関係なく、`catalog::Modifier`文字列内のコマンドを常に上書きします。

マクロはネストできますが、次の制限があります。マクロは、同じマクロ定義ファイル内の前の位置に現れるか、その埋め込みマクロの定義をデフォルトのマクロ定義ファイルに配置することで、マクロ定義が解析された時点で定義済みの場合にのみ呼び出すことができます。

同じ属性を異なる画像に適用する場合、マクロが役立ちます。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

共通属性のマクロを定義できます。

`view wid=240&fmt=pdf&imageRes=300`

このマクロは次のように使用されます。

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

`wid=`は3番目の要求とは異なるので、*の後の値*&#x200B;を上書きします（*`$view$`の前に`wid=`*&#x200B;を指定しても効果はありません）。

+ [name](r-name.md)
