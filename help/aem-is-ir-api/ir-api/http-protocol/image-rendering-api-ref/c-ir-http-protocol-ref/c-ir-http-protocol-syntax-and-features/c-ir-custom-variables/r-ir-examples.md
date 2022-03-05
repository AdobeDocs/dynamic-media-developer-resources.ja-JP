---
title: 例
description: この例では、画像サービングを使用してオブジェクトにカラーを付け、一連のビネットの 1 つにカスタムテキストを含むデカールを適用します。
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

この例では、画像サービングを使用してオブジェクトにカラーを付け、一連のビネットの 1 つにカスタムテキストを含むデカールを適用します。

IR 変数は、ビネット、ロゴ画像およびカスタムテキストを識別するために使用されます。

この `vignette::Modifier` 次の名前のレコードのフィールド *テンプレート* マテリアルカタログのビネットマップ内 `myCat` には次の情報が含まれます。

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

使用されたすべてのビネットは、マテリアルカタログのビネットマップに一覧表示されます `myCat`.

クライアントは、次のリクエストを実行して、デフォルト画像を取得できます（テンプレートの先頭で定義された変数を使用します）。

[!DNL `https://server/myCat/template`]

次のリクエストは、レンダリングする特定のコンテンツを指定します。

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

画像サービングについて詳しくは、画像サービングのドキュメントを参照してください `text=` コマンドを使用します。
