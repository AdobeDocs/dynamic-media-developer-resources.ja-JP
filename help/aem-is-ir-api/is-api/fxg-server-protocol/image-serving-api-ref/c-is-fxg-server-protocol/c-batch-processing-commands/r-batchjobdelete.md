---
description: ジョブの出力を削除します。
solution: Experience Manager
title: batchjobdelete
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

ジョブの出力を削除します。

ジョブが現在実行中の場合は、即座に停止され、そのすべての処理情報が削除されます。 ジョブが正常に完了した場合は、出力ファイルが削除されます。

このパラメーター：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>送信時に取得されたジョブID。 </p></td> 
 </tr> 
</table>

戻り値：

削除要求を受信した時点でのジョブのステータス。`jobid`が無効な場合、またはジョブが既に削除されている場合にエラーが発生します。

## 例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
