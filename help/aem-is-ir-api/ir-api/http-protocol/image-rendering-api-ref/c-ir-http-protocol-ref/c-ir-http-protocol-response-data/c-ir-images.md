---
description: 要求が正常に完了し、要求にreq=コマンドが含まれていない場合、またはreq=に次の値imgのいずれかが含まれている場合、イメージデータが返されます。
seo-description: 要求が正常に完了し、要求にreq=コマンドが含まれていない場合、またはreq=に次の値imgのいずれかが含まれている場合、イメージデータが返されます。
seo-title: 画像
solution: Experience Manager
title: 画像
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像{#images}

要求が正常に完了し、要求にreq=コマンドが含まれていない場合、またはreq=に次のいずれかの値が含まれている場合、画像データが返されます。img、debug

HTTP応答のMIMEタイプは、によって決ま `fmt=`ります。指定しな `fmt=` かった場合は、の値によって決まります `attribute::Format`。

リクエストメソッドが無条件またはの場合、HTTP応答ステータスは「200 OK」にな `GET` ります `HEAD`。

サーバはステータス「304」（変更なし）で応答し、（にフィールドがある）条件付きリクエストに応答してイメージデータを返さな `GET` い場合が [!DNL If-Modified-Since] あります(この場合 `request-header`は)。
