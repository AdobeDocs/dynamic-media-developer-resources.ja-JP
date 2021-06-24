---
description: 送信済みジョブの要約済みステータスの取得
solution: Experience Manager
title: batchjobbreifstatus
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# batchjobbreifstatus{#batchjobbriefstatus}

送信済みジョブの要約済みステータスの取得

このパラメーター：

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>送信時に取得されたジョブID。 </p> </td> 
 </tr> 
</table>

戻り値：

XML形式のジョブの簡単なステータス。ジョブidが無効な場合、またはジョブが削除された場合にエラーが発生します。

## 例 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
