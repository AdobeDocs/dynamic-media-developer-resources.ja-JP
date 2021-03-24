---
description: $var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。
solution: Experience Manager
title: ネストされたリクエストでの変数処理
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# 入れ子になったリクエスト{#variable-processing-in-nested-requests}での変数処理

$var$参照は、ネストされた画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）で囲まれた任意の場所に含まれます。 をクエリから切り離す。

サーバは、これらの参照を（メイン画像カタログのURLまたは`catalog::Modifier`からの）値で置き換えてから、ネストされた要求をさらに解析して処理します。

さらに、urlおよび`catalog::Modifier`のすべての`$ *[!DNL var]*=`定義が、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストのレベルに関係なく、1パスのHTTPエンコーディングのみを変数値に適用し、ネストされた画像レンダリングまたは画像サービング要求の任意の場所で置換する必要があります。
