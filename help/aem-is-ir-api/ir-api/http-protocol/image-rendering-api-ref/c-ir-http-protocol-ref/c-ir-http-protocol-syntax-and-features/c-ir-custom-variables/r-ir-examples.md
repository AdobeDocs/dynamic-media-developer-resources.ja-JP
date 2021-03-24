---
description: この例では、画像サービングを使用してオブジェクトに色を付け、ビネットのセットの1つにカスタムテキストを含むデカールを適用します。
solution: Experience Manager
title: 例
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# 例{#examples}

この例では、画像サービングを使用してオブジェクトに色を付け、ビネットのセットの1つにカスタムテキストを含むデカールを適用します。

IR変数は、ビネット、ロゴ画像、カスタムテキストを識別するために使用されます。

マテリアルカタログ`myCat`のビネットマップ内の&#x200B;*template*&#x200B;というレコード内の`vignette::Modifier`フィールドには、次の情報が含まれます。

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

使用されるビネットはすべて、マテリアルカタログ`myCat`のビネットマップに一覧表示されます。

クライアントは次のリクエストを行って、デフォルトの画像を取得できるようになりました（これはテンプレートの最初に定義された変数を使用します）。

[!DNL `https://server/myCat/template`]

次のリクエストは、レンダリングする特定のコンテンツを指定します。

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

画像サービング`text=`コマンドについて詳しくは、画像サービングのドキュメントを参照してください。
