---
description: 送信されたジョブの詳細なステータスを取得します。
solution: Experience Manager
title: batchjobdetaildstatus
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
