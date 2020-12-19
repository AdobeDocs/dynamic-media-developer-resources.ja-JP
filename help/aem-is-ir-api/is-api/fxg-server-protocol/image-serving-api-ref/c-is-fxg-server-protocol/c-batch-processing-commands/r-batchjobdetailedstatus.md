---
description: 送信されたジョブの詳細なステータスを取得します。
seo-description: 送信されたジョブの詳細なステータスを取得します。
seo-title: batchjobdetaildstatus
solution: Experience Manager
title: batchjobdetaildstatus
topic: Scene7 Image Serving - Image Rendering API
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

---


# batchjobdetailedstatus{#batchjobdetailedstatus}

送信されたジョブの詳細なステータスを取得します。

このパラメーター：

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>送信時に取得されたジョブID。 </p> </td> 
 </tr> 
</table>

戻り値：

XML形式のジョブの詳細なステータス。`jobid`が無効な場合、またはジョブが削除された場合にエラーが発生する。

## 例 {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
