---
description: $var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。
seo-description: $var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。
seo-title: ネストされたリクエストでの変数処理
solution: Experience Manager
title: ネストされたリクエストでの変数処理
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# 入れ子になったリクエスト{#variable-processing-in-nested-requests}での変数処理

$var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。

サーバは、これらの参照を（メイン画像カタログのURLまたは`catalog::Modifier`からの）値で置き換えてから、ネストされた要求をさらに解析して処理します。

さらに、urlおよび`catalog::Modifier`のすべての`$ *[!DNL var]*=`定義が、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストのレベルに関係なく、1パスのHTTPエンコーディングのみを変数値に適用し、ネストされた画像レンダリングまたは画像サービング要求の任意の場所で置換する必要があります。
