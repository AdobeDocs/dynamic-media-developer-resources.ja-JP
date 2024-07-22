---
title: 埋め込まれた外部リクエストの変数処理
description: 埋め込まれた外部リクエストの中カッコ内のどこかに存在する$var$参照は、対応する変数定義値に置き換えられます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 埋め込まれた外部リクエストの変数処理{#variable-processing-in-embedded-foreign-requests}

埋め込まれた外部リクエストの中カッコ内で使用される `$var$` 参照は、対応する変数定義値に置き換えられます。

埋め込まれた外部リクエストを画像カタログのテンプレートに配置できるようにします。

通常、外部リクエストに置き換える変数値はダブルエンコードする必要があります。これは、サーバーが最終的な外部 URL を送信しようとする前に再エンコードが適用されないからです。
