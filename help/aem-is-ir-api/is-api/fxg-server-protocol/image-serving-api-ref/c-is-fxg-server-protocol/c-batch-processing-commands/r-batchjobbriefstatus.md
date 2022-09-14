---
title: batchjobbreifstatus
description: 送信されたジョブの要約されたステータスを取得します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 13991f71ab54d1003a79a496b861d53a61899bdc
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---

# batchjobbreifstatus{#batchjobbriefstatus}

送信されたジョブの要約されたステータスを取得します。

このパラメーター：

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ジョブ </span> </p> </td> 
  <td class="stentry"> <p>送信時に取得されたジョブ ID。 </p> </td> 
 </tr> 
</table>

戻り値：

XML フォーマットのジョブの簡単なステータス。jobid が無効な場合、またはジョブが削除された場合にエラーが発生します。

## 例 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
