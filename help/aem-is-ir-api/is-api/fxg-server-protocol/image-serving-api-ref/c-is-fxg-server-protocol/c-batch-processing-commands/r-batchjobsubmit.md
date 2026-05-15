---
description: 新しいバッチジョブを送信します。
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
TQID: 'https://experienceleague.adobe.com/VJxy5jZsZC1MOo8LI5LSaMxtdDRqrFJSdqPXBRmBVvw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 38
ht-degree: 2%

---

# batchjobsubmit{#batchjobsubmit}

新しいバッチジョブを送信します。

このパラメーター：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ジョブ データ </span> </p> </td> 
  <td class="stentry"> <p>完全なジョブデータのXML スニペット。 </p> </td> 
 </tr> 
</table>

返品：

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>ジョブのステータス </p> </td> 
  <td class="stentry"> <p>送信が成功したか失敗したか。成功した場合は、XML形式のジョブ ID。 </p> </td> 
 </tr> 
</table>

## 例 {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
