---
description: $var$は、埋め込まれた外部リクエストの中括弧内の任意の場所で参照され、一致する変数定義値で置き換えられます。
seo-description: $var$は、埋め込まれた外部リクエストの中括弧内の任意の場所で参照され、一致する変数定義値で置き換えられます。
seo-title: 埋め込まれた外部要求での変数処理
solution: Experience Manager
title: 埋め込まれた外部要求での変数処理
topic: Scene7 Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 埋め込まれた外部要求での変数処理{#variable-processing-in-embedded-foreign-requests}

$var$は、埋め込まれた外部リクエストの中括弧内の任意の場所で参照され、一致する変数定義値で置き換えられます。

これにより、埋め込まれた外部リクエストを画像カタログのテンプレートに配置できます。

外部要求に置き換えられる変数値は、通常、二重エンコードする必要があります。これは、サーバーが最終的な外部URLの送信を試行する前に再エンコードが適用されないためです。
