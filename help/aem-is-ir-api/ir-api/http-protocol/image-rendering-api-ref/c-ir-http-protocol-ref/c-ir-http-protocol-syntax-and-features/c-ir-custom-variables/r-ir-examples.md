---
title: 例
description: この例では、画像サービングを使用してオブジェクトに色を付け、一連のビネットの 1 つにカスタムテキストを含むデカールを適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# 例{#examples}

この例では、画像サービングを使用してオブジェクトに色を付け、一連のビネットの 1 つにカスタムテキストを含むデカールを適用します。

IR 変数は、ビネット、ロゴ画像、カスタムテキストを識別するために使用されます。

マテリアル カタログ `myCat` のビネット マップの *template* という名前のレコードの `vignette::Modifier` フィールドには、次の項目が含まれます。

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

使用されたすべてのビネットは、マテリアル カタログ `myCat` のビネット マップに一覧表示されます。

クライアントは次のリクエストを実行して、デフォルトの画像を取得できるようになりました（テンプレートの先頭で定義した変数を使用します）。

[!DNL `https://server/myCat/template`]

次のリクエストでは、レンダリングする特定のコンテンツを指定します。

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

画像サービング `text=` コマンドについて詳しくは、画像サービングドキュメントを参照してください。
