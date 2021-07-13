---
description: $var$は、埋め込まれた外部リクエストの中括弧内の任意の場所にある参照を、一致する変数定義値に置き換えます。
solution: Experience Manager
title: 埋め込み外部リクエストでの変数処理
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# 埋め込み外部リクエストでの変数処理{#variable-processing-in-embedded-foreign-requests}

$var$は、埋め込まれた外部リクエストの中括弧内の任意の場所にある参照を、一致する変数定義値に置き換えます。

これにより、埋め込まれた外部リクエストを画像カタログのテンプレートに配置できます。

変数値で外部要求に置き換える場合は、通常、二重エンコードする必要があります。これは、サーバーが最終的な外部URLを送信しようとする前に再エンコードが適用されないからです。
