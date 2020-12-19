---
description: 標準アラートは、設定された平均化間隔の終わりに、統合された電子メールメッセージと共に送信されます。
seo-description: 標準アラートは、設定された平均化間隔の終わりに、統合された電子メールメッセージと共に送信されます。
seo-title: 標準アラート
solution: Experience Manager
title: 標準アラート
topic: Scene7 Image Serving - Image Rendering API
uuid: d3294434-a44b-4742-9d77-a6945760d33c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---


# 標準アラート{#standard-alerts}

標準アラートは、設定された平均化間隔の終わりに、統合された電子メールメッセージと共に送信されます。

次の表に、標準アラートの各タイプを示します。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>アラートタイプ</b> </th> 
   <th class="entry"> <b>タイトルID</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>ロックされた要求 </p> </td> 
   <td> <p>ロック </p> </td> 
   <td> <p>リクエストが指定したしきい値内にクライアントに応答を返さなかった場合に送信されます。 ハングした要求を示す可能性があり、Javaスレッドプールの空乏化の原因になる可能性があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高い並行性 </p> </td> 
   <td> <p>コンク </p> </td> 
   <td> 同時に処理されるリクエストの数（<i>重複</i>）が、指定したしきい値を超えると発生します。 サーバーの過負荷状態を示す可能性があります。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小トラフィック </p> </td> 
   <td> <p>トラフ </p> </td> 
   <td> <p>要求全体の速度が指定したしきい値を下回った場合に生成されます。 通常は、サーバーの通信に関する問題を示します（例：サーバーがオフラインになった場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>エラー率 </p> </td> 
   <td> <p>エラー </p> </td> 
   <td> <p>サンプリング間隔中のHTTPエラー応答の平均レートが指定したしきい値を超えた場合に発生します。 設定上の問題、画像が見つからない、Webサイトのプログラミングやデータベースのエラーを示す可能性があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>応答時間 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>サンプリング間隔中の平均リクエスト処理時間が、指定したしきい値を超えた場合に送信されます。 通常は、サーバまたはバックエンドイメージストレージシステムの一時的な過負荷状態または持続的な過負荷状態を示します。 </p> <p>平均応答時間を計算する際には、エラー応答は考慮されません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

