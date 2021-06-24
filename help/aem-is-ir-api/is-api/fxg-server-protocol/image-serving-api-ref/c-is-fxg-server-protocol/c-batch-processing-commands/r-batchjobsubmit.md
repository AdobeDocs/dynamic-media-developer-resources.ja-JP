---
description: 新しいバッチジョブを送信します。
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '43'
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
