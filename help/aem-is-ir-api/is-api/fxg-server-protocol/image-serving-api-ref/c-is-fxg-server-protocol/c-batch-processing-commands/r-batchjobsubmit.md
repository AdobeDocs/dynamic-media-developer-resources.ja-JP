---
description: 新しいバッチジョブを送信します。
seo-description: 新しいバッチジョブを送信します。
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Scene7 Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobsubmit{#batchjobsubmit}

新しいバッチジョブを送信します。

このパラメータ：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata </span> </p> </td> 
  <td class="stentry"> <p>ジョブ完了データのXMLスニペット。 </p> </td> 
 </tr> 
</table>

戻り値：

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>ジョブのステータス </p> </td> 
  <td class="stentry"> <p>送信が成功したか失敗したか。成功した場合、XML形式のジョブID。 </p> </td> 
 </tr> 
</table>

## 例 {#section-3886e8352e26419c97b24df21ca7f6fd}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&amp;jobdata=<URLEncodedXMLFileContents>]
