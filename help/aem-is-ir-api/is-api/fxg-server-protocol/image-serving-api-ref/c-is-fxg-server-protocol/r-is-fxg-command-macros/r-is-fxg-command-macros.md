---
title: コマンド マクロ
description: コマンド マクロは、コマンドのセットに名前付きショートカットを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# コマンド マクロ{#command-macros}

コマンド マクロは、コマンドのセットに名前付きショートカットを提供します。

マクロは、個別のマクロ定義ファイルで定義され、イメージ カタログまたは既定のカタログにアタッチできます。

マクロは、リクエスト内の「?」より後の任意の場所、および `catalog::Modifier` フィールド内の任意の場所で呼び出すことができます。 マクロは、1 つ以上の完全な画像サービングコマンドしか表現できません。したがって、修飾子文字列の先頭または末尾にある場合を除き、&#39;&amp;&#39;区切り記号で囲む必要があります。

マクロ呼び出しは、解析中に置換文字列に置き換えられます。 マクロ内のコマンドは、リクエスト内のマクロ呼び出しの前に発生した場合、リクエスト内の同じコマンドを上書きします。 このフローは `catalog::Modifier` とは異なります。リクエスト内の位置に関係なく、リクエスト文字列内のコマンドは常にリクエスト文字列 `catalog::Modifier` のコマンドを上書きします。

マクロはネストできます。 ただし、マクロ定義の解析時に既に定義されている場合にのみ、マクロを呼び出すことができます。 このフローは、同じマクロ定義ファイルの前に表示するか、埋め込まれたマクロの定義をデフォルトのマクロ定義ファイルに配置することによって実行されます。

マクロは、同じ属性を異なる画像に適用する場合に役立ちます。

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

共通の属性用のマクロを定義できます。

`view wid=240&fmt=pdf&imageRes=300`

マクロは次のように使用されます。

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

3 回目のリクエストでは `wid=` が異なるので、マクロが呼び出される *after* の値を上書きするだけです（`wid=`*before*`$view$` を指定しても効果はありません）。

+ [name](r-name.md)
