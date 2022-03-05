---
title: 埋め込まれた外部リクエストでの変数処理
description: $var$は、埋め込まれた外部リクエストの中括弧内で発生する参照を、一致する変数定義値に置き換えます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 埋め込まれた外部リクエストでの変数処理{#variable-processing-in-embedded-foreign-requests}

任意 `$var$` 埋め込まれた外部リクエストの中括弧内で発生する参照は、一致する変数定義値に置き換えられます。

埋め込まれた外部リクエストを画像カタログのテンプレートに配置できるようにします。

外部要求で置き換えられる変数の値は、通常、二重エンコードする必要があります。サーバーが最終的な外部 URL を送信しようとする前に再エンコードが適用されないからです。
