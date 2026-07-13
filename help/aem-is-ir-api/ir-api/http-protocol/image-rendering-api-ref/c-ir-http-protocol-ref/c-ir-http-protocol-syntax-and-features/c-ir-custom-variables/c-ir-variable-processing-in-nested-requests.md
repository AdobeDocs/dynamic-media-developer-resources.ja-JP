---
title: ネストされたリクエストでの変数処理
description: $var$参照は、ネストされた画像サービングまたは画像レンダリングリクエストの中括弧の中のどこでも発生する可能性があります。これには、クエリからパスを分離する「?」の左側も含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# ネストされたリクエストでの変数処理{#variable-processing-in-nested-requests}

$var$参照は、ネストされた画像サービングまたは画像レンダリングリクエストの中括弧の中のどこでも発生する可能性があります。これには、クエリからパスを分離する「?」の左側も含まれます。

サーバーは、ネストされたリクエストをさらに解析して処理する前に、これらの参照を値（URLまたはメイン画像カタログの`catalog::Modifier`から）に置き換えます。

さらに、URLおよび`catalog::Modifier`からのすべての`$ *[!DNL var]*=`定義は、ネストされたすべての画像サービングおよび画像レンダリング要求に転送されます。 これにより、ネスト レベルに関係なく、すべての変数定義がすべてのテンプレートで使用できるようになります。

ネスティングレベルに関係なく、単一パス HTTP エンコーディングのみを、ネストされた画像レンダリングまたは画像サービング要求のどこでも置換される変数値に適用する必要があります。

