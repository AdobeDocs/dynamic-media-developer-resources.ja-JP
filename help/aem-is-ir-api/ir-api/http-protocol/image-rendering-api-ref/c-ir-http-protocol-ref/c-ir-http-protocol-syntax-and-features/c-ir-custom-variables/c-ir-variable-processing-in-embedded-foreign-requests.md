---
description: $var$では、埋め込まれた外部要求の中括弧内にある参照は、対応する変数定義値に置き換えられます。
seo-description: $var$では、埋め込まれた外部要求の中括弧内にある参照は、対応する変数定義値に置き換えられます。
seo-title: 埋め込まれた外部要求での変数処理
solution: Experience Manager
title: 埋め込まれた外部要求での変数処理
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# 埋め込まれた外部要求での変数処理{#variable-processing-in-embedded-foreign-requests}

$var$では、埋め込まれた外部要求の中括弧内にある参照は、対応する変数定義値に置き換えられます。

これにより、埋め込まれた外部要求を画像カタログのテンプレートに配置できます。

外部要求で置き換えられる変数値は、通常、重複エンコードする必要があります。これは、サーバーが最終的な外部URLの送信を試行する前に再エンコードが適用されないためです。
