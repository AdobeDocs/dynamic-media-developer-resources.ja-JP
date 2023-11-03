---
description: 標準アラートは、設定された平均化間隔の終わりに統合された E メールメッセージと共に送信されます。
solution: Experience Manager
title: 標準アラート
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 標準アラート{#standard-alerts}

標準アラートは、設定された平均化間隔の終わりに統合された E メールメッセージと共に送信されます。

次の表に、標準アラートの各タイプを示します。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>アラートタイプ</b> </th> 
   <th class="entry"> <b>タイトル ID</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>ロックされたリクエスト </p> </td> 
   <td> <p>ロック </p> </td> 
   <td> <p>リクエストが、指定されたしきい値内でクライアントに応答を返さなかった場合に送信されます。 ハングしたリクエストを示す可能性があり、Java スレッドプールの空乏化を引き起こす可能性があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高い同時実行性 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 同時に処理されるリクエストの数 ( <i>重複</i>) が指定されたしきい値を超えています。 サーバーの過負荷状態を示す可能性があります。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小トラフィック </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>全体のリクエスト率が指定したしきい値を下回った場合に生成されます。 通常は、サーバーの通信の問題を示します（例えば、サーバーが回線から外れた場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>エラー率 </p> </td> 
   <td> <p>エラー </p> </td> 
   <td> <p>サンプリング間隔中の HTTP エラー応答の平均レートが指定したしきい値を超えた場合に発生します。 設定の問題、画像の欠落、Web サイトのプログラミングやデータベースのエラーを示す可能性があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>応答時間 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>サンプリング間隔中の平均リクエスト処理時間が指定したしきい値を超えた場合に送信されます。 通常は、サーバまたはバックエンドのイメージストレージシステムの一時的または永続的な過負荷状態を示します。 </p> <p>平均応答時間を計算する際に、エラー応答は考慮されません。 </p> </td> 
  </tr> 
 </tbody> 
</table>
