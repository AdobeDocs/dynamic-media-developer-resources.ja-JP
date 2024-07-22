---
title: 画像
description: リクエストが正常に完了し、リクエストに req= コマンドが含まれていない場合、または req=に次の値のいずれかが含まれている場合、画像データが返されます（img、debug）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# 画像{#images}

リクエストが正常に完了し、リクエストに req= コマンドが含まれていない場合、または req=に img や debug のいずれかの値がある場合、画像データが返されます。

HTTP 応答の MIME タイプは、`fmt=` によって決定されます。`fmt=` が指定されていない場合は、`attribute::Format` の値によって決定されます。

リクエストメソッドが無条件の `GET` または `HEAD` の場合、HTTP 応答のステータスは「200 OK」です。

サーバーは、ステータス「304」（変更されていない）で応答し、条件付きの `GET` リクエストに応答して画像データを返さない場合があります（`request-header` に [!DNL If-Modified-Since] フィールドが存在する）。
