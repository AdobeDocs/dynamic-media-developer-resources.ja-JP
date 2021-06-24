---
description: $var$参照は、ネストされた画像サービング要求または画像レンダリング要求の中括弧内の任意の場所で、「?」の左側を含めて発生する可能性があります。 クエリからパスを分離する。
solution: Experience Manager
title: ネストされたリクエストでの変数処理
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# ネストされたリクエストでの変数処理{#variable-processing-in-nested-requests}

$var$参照は、ネストされた画像サービング要求または画像レンダリング要求の中括弧内の任意の場所で、「?」の左側を含めて発生する可能性があります。 クエリからパスを分離する。

サーバーは、ネストされた要求をさらに解析および処理する前に、これらの参照を(メイン画像カタログのURLまたは`catalog::Modifier`の値で置き換えます。

さらに、URLと`catalog::Modifier`のすべての`$ *[!DNL var]*=`定義が、ネストされたすべての画像サービング要求と画像レンダリング要求に転送されます。 これにより、ネストレベルに関係なく、すべてのテンプレートですべての変数定義を使用できます。

ネストのレベルに関係なく、単一パスのHTTPエンコーディングのみを変数値に適用し、ネストされた画像レンダリング要求または画像サービング要求の任意の場所で置き換える必要があります。
