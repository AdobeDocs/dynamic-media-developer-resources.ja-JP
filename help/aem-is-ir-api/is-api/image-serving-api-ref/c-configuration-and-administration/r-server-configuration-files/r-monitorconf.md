---
description: 監視/警告システムの設定が含まれます。
solution: Experience Manager
title: monitor.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 09c30680-dd9f-4744-b5ec-105721058883
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# monitor.conf{#monitor-conf}

監視/警告システムの設定が含まれます。

このファイルは、JAVA プロパティファイルです。 適切な規則に従うように注意しなければならない。それ以外の場合は [!DNL Platform Server] を開始できない可能性があります。 このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されるので、Windows のファイルパスでは、バックスラッシュ&#39;\\&#39;の代わりに、二重のバックスラッシュ&#39;\\&#39;または 1 つのフォワードスラッシュ&#39;/&#39;を使用する必要があります。

このファイルに対する変更は、ファイルが保存された直後に有効になります。

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1 </span> </p> <p> <span class="codeph"> mailSender.port=25 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>アラートしきい値 </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>
