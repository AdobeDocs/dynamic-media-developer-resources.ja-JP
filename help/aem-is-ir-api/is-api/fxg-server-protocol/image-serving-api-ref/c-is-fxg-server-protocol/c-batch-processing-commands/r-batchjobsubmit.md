---
description: 新しいバッチジョブを送信します。
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 2%

---


# batchjobsubmit{#batchjobsubmit}

新しいバッチジョブを送信します。

このパラメーター：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>完全なジョブデータのXMLスニペット。 </p> </td> 
 </tr> 
</table>

戻り値：

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>ジョブの状態 </p> </td> 
  <td class="stentry"> <p>送信が成功したか失敗したか。成功した場合は、XML形式のジョブID。 </p> </td> 
 </tr> 
</table>

## 例 {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
