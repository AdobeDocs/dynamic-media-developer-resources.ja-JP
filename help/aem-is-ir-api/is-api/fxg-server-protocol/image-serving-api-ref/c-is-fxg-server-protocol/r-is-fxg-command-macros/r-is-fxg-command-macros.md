---
title: コマンドマクロ
description: コマンドマクロは、一連のコマンドに名前付きショートカットを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
TQID: 'https://experienceleague.adobe.com/DbXn35KC7OLFI0Dulgobj3UFPHnubmCisNDS541j8lE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 248
ht-degree: 0%

---

# コマンドマクロ{#command-macros}

コマンドマクロは、一連のコマンドに名前付きショートカットを提供します。

マクロは個別のマクロ定義ファイルで定義され、画像カタログまたはデフォルトカタログに添付できます。

マクロは、「?」の後のリクエスト内の任意の場所、および`catalog::Modifier` フィールド内の任意の場所で呼び出すことができます。 マクロは、1つ以上の完全な画像サービングコマンドのみを表すことができるため、「&amp;」区切り記号で囲む必要があります（修飾子文字列の先頭または末尾にある場合を除く）。

マクロ呼び出しは、パースの早い段階で代用文字列に置き換えられます。 マクロ内のコマンドは、リクエスト内のマクロ呼び出しの前に発生した場合、リクエスト内の同じコマンドを上書きします。 このフローは、`catalog::Modifier`とは異なります。リクエスト文字列内のコマンドは、リクエスト内の位置に関係なく、`catalog::Modifier`文字列内のコマンドを常に上書きします。

マクロはネストできます。 ただし、マクロは、マクロ定義の解析時に既に定義されている場合にのみ呼び出すことができます。 このフローは、同じマクロ定義ファイル内で以前に表示するか、そのような埋め込みマクロの定義をデフォルトのマクロ定義ファイルに配置することで実行されます。

マクロは、同じ属性を異なる画像に適用する場合に便利です。

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

共通の属性のマクロを定義できます。

`view wid=240&fmt=pdf&imageRes=300`

マクロは次のように使用されます。

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

`wid=`は3番目のリクエストとは異なるため、マクロが呼び出された&#x200B;*後*&#x200B;の値を上書きするだけです（`wid=` *前* `$view$`を指定しても効果はありません）。

+ [name](r-name.md)
