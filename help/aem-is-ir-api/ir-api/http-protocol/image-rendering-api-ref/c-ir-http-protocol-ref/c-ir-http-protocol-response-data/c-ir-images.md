---
title: 画像
description: イメージデータは、リクエストが正常に完了し、リクエストに req=コマンドが含まれていない場合、または req=に次の値のいずれかが含まれている場合、デバッグを返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# 画像{#images}

イメージデータは、リクエストが正常に完了し、リクエストに req=コマンドが含まれていない場合、または req=に次の値のいずれかが含まれている場合に返されます。img, debug

HTTP 応答の MIME タイプは、 `fmt=`、または `fmt=` が指定されていない場合は、 `attribute::Format`.

リクエストメソッドが無条件の場合、HTTP 応答ステータスは「200 OK」です `GET` または `HEAD`.

サーバーは、ステータス「304」（未変更）で返信し、条件付きに応じて画像データを返さない場合があります `GET` リクエスト ( [!DNL If-Modified-Since] に存在するフィールド `request-header`) をクリックします。
