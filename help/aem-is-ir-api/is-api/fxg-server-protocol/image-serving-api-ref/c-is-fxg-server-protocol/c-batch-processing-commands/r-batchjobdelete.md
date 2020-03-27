---
description: ジョブの出力を削除します。
seo-description: ジョブの出力を削除します。
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdelete{#batchjobdelete}

ジョブの出力を削除します。

ジョブが現在実行中の場合、ジョブは直ちに停止され、そのすべての処理情報が削除されます。 ジョブが正常に完了した場合、出力ファイルは削除されます。

このパラメータ：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>送信時に取得されたジョブID。 </p></td> 
 </tr> 
</table>

戻り値：

削除要求を受け取った時点のジョブのステータス。無効な場合、またはジョ `jobid` ブが既に削除されている場合はエラーです。

## 例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
