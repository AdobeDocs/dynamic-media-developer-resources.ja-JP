---
description: $var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。
seo-description: $var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。
seo-title: ネストされたリクエストでの変数処理
solution: Experience Manager
title: ネストされたリクエストでの変数処理
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# 入れ子になったリクエスト{#variable-processing-in-nested-requests}での変数処理

$var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。

サーバは、これらの参照を（メイン画像カタログのURLまたは`catalog::Modifier`からの）値で置き換えてから、ネストされた要求をさらに解析して処理します。

さらに、urlおよび`catalog::Modifier`のすべての`$ *[!DNL var]*=`定義が、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストのレベルに関係なく、1パスのHTTPエンコーディングのみを変数値に適用し、ネストされた画像レンダリングまたは画像サービング要求の任意の場所で置換する必要があります。
