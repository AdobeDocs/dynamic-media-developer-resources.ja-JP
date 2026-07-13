---
title: 例
description: この例では、画像サービングを使用して、オブジェクトに色を付け、一連のビネットの1つにカスタムテキストを含むデカールを適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
TQID: 'https://experienceleague.adobe.com/GMzKDuP-wzTrPJQbxpXc0M08BjCQdWCkGo5jOUiWipU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 1%

---

# 例{#examples}

この例では、画像サービングを使用して、オブジェクトに色を付け、一連のビネットの1つにカスタムテキストを含むデカールを適用します。

IR変数は、周辺光量補正、ロゴ画像、およびカスタムテキストを識別するために使用されます。

材料カタログ `myCat`の周辺光量補正マップの&#x200B;*テンプレート*&#x200B;という名前のレコードの`vignette::Modifier` フィールドには、次のものが含まれています。

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

使用されているすべてのビネットは、マテリアル カタログ `myCat`のビネット マップに一覧表示されます。

クライアントは、デフォルトの画像を取得するために次のリクエストを実行できるようになりました（テンプレートの先頭で定義された変数を使用します）。

[!DNL `https://server/myCat/template`]

次のリクエストは、レンダリングする特定のコンテンツを指定します。

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Image Serving `text=` コマンドについて詳しくは、Image Serving Documentationを参照してください。

