---
title: ネストされたリクエストでの変数処理
description: $var$参照は、「?」の左側を含め、ネストされた画像サービングまたは画像レンダリング要求の中括弧内の任意の場所で発生する場合があります。 クエリからパスを分離する
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# ネストされたリクエストでの変数処理{#variable-processing-in-nested-requests}

$var$参照は、「?」の左側を含め、ネストされた画像サービングまたは画像レンダリング要求の中括弧内の任意の場所で発生する場合があります。 クエリからパスを分離する

サーバーは、これらの参照を (URL または `catalog::Modifier` （メイン画像カタログの）) ネストされたリクエストをさらに解析および処理する前に呼び出します。

さらに、 `$ *[!DNL var]*=` url からの定義と `catalog::Modifier` は、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべての変数定義をすべてのテンプレートで使用できるようになります。

ネストのレベルに関係なく、ネストされた画像レンダリング要求または画像サービング要求の任意の場所で置き換える変数値には、シングルパス HTTP エンコーディングのみを適用する必要があります。
