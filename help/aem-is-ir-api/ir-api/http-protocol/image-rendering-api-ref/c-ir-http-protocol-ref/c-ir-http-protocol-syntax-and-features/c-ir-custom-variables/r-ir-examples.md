---
description: この例では、画像サービングを使用してオブジェクトに色を付け、ビネットのセットの1つにカスタムテキストを含むデカールを適用します。
solution: Experience Manager
title: 例
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 1%

---

# 例{#examples}

この例では、画像サービングを使用してオブジェクトに色を付け、ビネットのセットの1つにカスタムテキストを含むデカールを適用します。

IR変数は、ビネット、ロゴ画像およびカスタムテキストを識別するために使用されます。

マテリアルカタログ`myCat`のビネットマップ内の&#x200B;*template*&#x200B;というレコード内の`vignette::Modifier`フィールドには、次の値が含まれます。

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

使用されるすべてのビネットは、マテリアルカタログ`myCat`のビネットマップにリストされます。

クライアントは、次のリクエストを実行して、デフォルト画像を取得できるようになりました（これは、テンプレートの最初に定義された変数を使用します）。

[!DNL `https://server/myCat/template`]

次のリクエストは、レンダリングする特定のコンテンツを指定します。

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

画像サービングの`text=`コマンドについて詳しくは、画像サービングのドキュメントを参照してください。
