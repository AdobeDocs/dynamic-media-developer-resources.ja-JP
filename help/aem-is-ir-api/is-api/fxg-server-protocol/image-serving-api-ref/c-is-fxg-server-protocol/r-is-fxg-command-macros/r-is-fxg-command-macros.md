---
title: コマンドマクロ
description: コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。

マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは既定のカタログにアタッチできます。

マクロは、リクエスト内の「?」より後の任意の場所、および `catalog::Modifier` フィールドに入力します。 マクロは 1 つ以上の画像サービングコマンドのみを表すので、アンパサーで囲む必要があります（修飾子文字列の先頭または末尾を除く）。

マクロの呼び出しは、解析の初期段階で置き換え文字列に置き換えられます。 マクロ内のコマンドは、要求でマクロが呼び出される前に発生した場合、要求内の同じコマンドを上書きします。 このフローは、 `catalog::Modifier`( リクエスト文字列のコマンドは常に `catalog::Modifier` 文字列を指定します。

マクロはネストできます。 ただし、マクロは、マクロ定義が解析された時点で既に定義されている場合にのみ呼び出すことができます。 このフローは、同じマクロ定義ファイル内で既に表示されているか、埋め込まれたマクロの定義を既定のマクロ定義ファイル内に配置することで実行されます。

マクロは、異なる画像に同じ属性を適用する場合に役立ちます。

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

次の共通属性のマクロを定義できます。

`view wid=240&fmt=pdf&imageRes=300`

このマクロは次のように使用されます。

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

理由： `wid=` が 3 番目のリクエストと異なる場合は、単に *次より後* マクロが呼び出されます ( `wid=` *前* `$view$` には何の効果もありません )。

+ [name](r-name.md)
