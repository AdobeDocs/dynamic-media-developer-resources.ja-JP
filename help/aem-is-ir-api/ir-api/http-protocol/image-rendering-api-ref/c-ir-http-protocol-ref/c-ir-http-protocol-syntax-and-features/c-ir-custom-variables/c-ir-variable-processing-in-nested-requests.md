---
title: ネストされたリクエストでの変数の処理
description: $var$参照は、「?」の左側を含め、ネストされた画像サービングまたは画像レンダリングリクエストの中括弧のどこかに存在する可能性があります。 パスとクエリを分離しています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# ネストされたリクエストでの変数の処理{#variable-processing-in-nested-requests}

$var$参照は、「?」の左側を含め、ネストされた画像サービングまたは画像レンダリングリクエストの中括弧のどこかに存在する可能性があります。 パスとクエリを分離しています。

サーバーは、ネストされたリクエストをさらに解析して処理する前に、これらの参照を（url またはメイン画像カタログの `catalog::Modifier` から）値に置き換えます。

さらに、URL および `catalog::Modifier` からのすべての `$ *[!DNL var]*=` 定義は、ネストされたすべての画像サービングおよび画像レンダリングリクエストに転送されます。 これにより、ネストレベルに関係なく、すべての変数定義をすべてのテンプレートで使用できるようになります。

ネストのレベルに関係なく、ネストされた画像レンダリングまたは画像サービングリクエストの任意の場所で置き換える変数値には、シングルパス HTTP エンコーディングのみを適用します。
