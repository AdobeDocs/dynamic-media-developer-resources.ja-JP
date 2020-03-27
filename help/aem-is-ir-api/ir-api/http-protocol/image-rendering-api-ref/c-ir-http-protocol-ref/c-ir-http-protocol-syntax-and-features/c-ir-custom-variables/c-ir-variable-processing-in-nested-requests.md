---
description: $var$参照は、入れ子になった画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）の任意の場所で使用できます。 パスをクエリーから分離する。
seo-description: $var$参照は、入れ子になった画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）の任意の場所で使用できます。 パスをクエリーから分離する。
seo-title: ネストされたリクエストでの変数処理
solution: Experience Manager
title: ネストされたリクエストでの変数処理
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ネストされたリクエストでの変数処理{#variable-processing-in-nested-requests}

$var$参照は、入れ子になった画像サービングまたは画像レンダリング要求の中括弧内（「?」の左を含む）の任意の場所で使用できます。 パスをクエリーから分離する。

サーバーは、ネストされた要求をさらに解析して処理する前に、これらの参照を値(URLまたはメ `catalog::Modifier` イン画像カタログの値)で置き換えます。

さらに、URLからのすべての定 `$ *[!DNL var]*=` 義が、ネストされたす `catalog::Modifier` べての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストレベルに関係なく、単一パスのHTTPエンコーディングのみを変数値に適用し、これらの値はネストされた画像レンダリングまたは画像サービング要求の任意の場所で置き換える必要があります。
