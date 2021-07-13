---
description: 送信済みジョブの詳細ステータスの取得
solution: Experience Manager
title: batchjobdetailedstatus
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: fd385327-29af-448c-9a25-75098b578272
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 1%

---

# batchjobdetailedstatus{#batchjobdetailedstatus}

送信済みジョブの詳細ステータスの取得

このパラメーター：

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>送信時に取得されたジョブID。 </p> </td> 
 </tr> 
</table>

戻り値：

XML形式のジョブの詳細なステータス。`jobid`が無効な場合、またはジョブが削除された場合にエラーが発生します。

## 例 {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
