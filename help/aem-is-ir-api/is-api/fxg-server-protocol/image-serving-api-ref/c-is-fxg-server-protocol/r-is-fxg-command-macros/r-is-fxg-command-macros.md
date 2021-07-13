---
description: コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。
solution: Experience Manager
title: コマンドマクロ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、コマンドのセットの名前付きショートカットを提供します。

マクロは、個別のマクロ定義ファイルで定義され、画像カタログまたは既定のカタログに添付できます。

マクロは、リクエスト内の「?」より後の任意の場所、および`catalog::Modifier`フィールド内の任意の場所で呼び出すことができます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表すことができるので、「&amp;」区切り文字で囲む必要があります（修飾子文字列の先頭または末尾を除く）。

マクロの呼び出しは、解析の初期段階で置換文字列に置き換えられます。 マクロ内のコマンドは、リクエストでマクロを呼び出す前に発生した場合、リクエスト内の同じコマンドを上書きします。 これは`catalog::Modifier`とは異なります。要求文字列内のコマンドは、要求内の位置に関係なく、常に`catalog::Modifier`文字列内のコマンドを上書きします。

マクロはネストでき、次の制限があります。マクロは、マクロ定義が解析された時点で定義済みの場合にのみ呼び出すことができます。同じマクロ定義ファイル内に既に存在する場合や、その埋め込みマクロの定義を既定のマクロ定義ファイルに配置する場合です。

マクロは、同じ属性を異なる画像に適用する場合に役立ちます。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

共通の属性に対してマクロを定義できます。

`view wid=240&fmt=pdf&imageRes=300`

このマクロは次のように使用されます。

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

3番目のリクエストでは`wid=`が異なるので、マクロが呼び出された後の値&#x200B;**&#x200B;を上書きします（`wid=`*before* `$view$`を指定しても効果はありません）。

+ [name](r-name.md)
