---
description: 要求が正常に完了し、要求にreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合は、画像データが返されます。
seo-description: 要求が正常に完了し、要求にreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合は、画像データが返されます。
seo-title: 画像
solution: Experience Manager
title: 画像
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像{#images}

要求が正常に完了し、要求にreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合は、画像データが返されます。

HTTP応答のMIMEタイプは、によって決ま `fmt=`ります。指定しな `fmt=` かった場合は、指定しま `<image/jpeg>`す。

リクエストメソッドが無条件またはの場合、HTTP応答ステータスは「200 OK」にな `GET` ります `HEAD`。

サーバーはステータス「304」（変更なし）で応答し、（有効なまたはヘッダーを含む）条件付き要求に応答して画像デ `GET` ータを返さない場合が `If-Modified-Since` あり `If-None-Match` ます。
