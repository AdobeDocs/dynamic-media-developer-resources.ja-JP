---
description: この例では、画像サービングを使用して、オブジェクトの色を付け、ビネットのセットの1つにカスタムテキストを含むデカルを適用します。
seo-description: この例では、画像サービングを使用して、オブジェクトの色を付け、ビネットのセットの1つにカスタムテキストを含むデカルを適用します。
seo-title: 例
solution: Experience Manager
title: 例
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# 例{#examples}

この例では、画像サービングを使用して、オブジェクトの色を付け、ビネットのセットの1つにカスタムテキストを含むデカルを適用します。

IR変数は、ビネット、ロゴ画像、カスタムテキストを識別するために使用されます。

マテリアル `vignette::Modifier` カタログのビネットマップ内の *template* というレコード内のフィールドには、次 `myCat` のものが含まれます。

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

使用されるビネットはすべて、マテリアルカタログのビネットマップに一覧表示されま `myCat`す。

クライアントは、次のリクエストを行って、デフォルトの画像を取得できるようになりました（テンプレートの最初に定義された変数を使用します）。

[!DNL `https://server/myCat/template`]

次のリクエストは、レンダリングする特定のコンテンツを指定します。

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

画像サービングコマンドについて詳しくは、画像サービングのドキュメントを参照して `text=` ください。
