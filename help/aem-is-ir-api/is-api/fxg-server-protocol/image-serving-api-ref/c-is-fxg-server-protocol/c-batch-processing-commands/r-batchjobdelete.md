---
title: batchjobdelete
description: ジョブの出力を削除します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

ジョブの出力を削除します。

ジョブが現在実行中の場合は、即座に停止され、その処理情報がすべて削除されます。 ジョブが正常に完了した場合、その出力ファイルは削除されます。

このパラメーター：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>送信時に取得されたジョブ ID。 </p></td> 
 </tr> 
</table>

戻り値：

削除リクエストを受信した時点でのジョブのステータス（次の場合にエラー） `jobid` は無効か、ジョブは既に削除されています。

## 例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
