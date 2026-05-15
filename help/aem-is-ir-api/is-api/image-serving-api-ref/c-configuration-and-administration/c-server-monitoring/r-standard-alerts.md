---
description: 標準アラートは、設定された平均化間隔の最後に、統合メールメッセージとともに送信されます。
solution: Experience Manager
title: 標準アラート
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
TQID: 'https://experienceleague.adobe.com/EJzmjshgrIk8hpvZvljpsWTHSI-mG67UNAg2NVjBcZg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 0%

---

# 標準アラート{#standard-alerts}

標準アラートは、設定された平均化間隔の最後に、統合メールメッセージとともに送信されます。

次の表に、標準アラートの各タイプを示します。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> アラートの種類</b> </th> 
   <th class="entry"> <b> タイトル Id</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>ロックされたリクエスト </p> </td> 
   <td> <p>ロック </p> </td> 
   <td> <p>リクエストが、指定されたしきい値内のクライアントに応答を返すことができない場合に送信されます。 Java スレッドプールの枯渇を引き起こす可能性がある、ハングしたリクエストを示すことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>同時視聴数の増加 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 同時に処理されるリクエストの数（<i>重複</i>）が、指定されたしきい値を超えた場合に発行されます。 サーバーの過負荷状態を示すことができます。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小トラフィック </p> </td> 
   <td> <p>トラフ </p> </td> 
   <td> <p>全体のリクエストレートが指定されたしきい値を下回ったときに生成されます。 通常、サーバーの通信に関する問題（サーバーがオフラインになった場合など）を示します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>エラー率 </p> </td> 
   <td> <p>エラー </p> </td> 
   <td> <p>サンプリング間隔におけるHTTP エラー応答の平均レートが、指定されたしきい値を超えた場合に発行されます。 設定の問題、画像の欠落、web サイトのプログラミングまたはデータベースのエラーを示すことができます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>応答時間 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>サンプリング間隔の平均要求処理時間が、指定されたしきい値を超えて増加したときに送信されます。 通常、サーバーまたはバックエンドの画像ストレージシステムの一時的または永続的な過負荷状態を示します。 </p> <p>平均応答時間を計算する場合、エラー応答は考慮されません。 </p> </td> 
  </tr> 
 </tbody> 
</table>
