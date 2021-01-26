---
description: タスクの進行状況の情報。
seo-description: タスクの進行状況の情報。
seo-title: TaskProgress
solution: Experience Manager
title: TaskProgress
topic: Dynamic Media Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---


# TaskProgress{#taskprogress}

タスクの進行状況の情報。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> タスクタイプの説明。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 既に処理済みのタスク項目数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 現在処理中のタスク項目数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 保留中のタスク項目（まだ処理されていません）の数です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 進行状況</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:重複</span> </td> 
   <td colname="col3"> %進行状況(0.0 ～ 1.0) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 進行状況のメッセージ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 前回の進行状況情報が最後に更新された時刻。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：TaskItemProgressArray</span> </td> 
   <td colname="col3"> タスク項目の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">次の値があります。 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> 不明</span>:タスクが状態間のトランジションを監視したとき。 </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> 新規</span>:タスクモニタは作成されましたが、まだタスクを受け入れていません。 </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> 処理</span>:タスクモニターは、タスクをアクティブに処理しています。 </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> 停止中</span>:ジョブの停止要求が原因で、タスクモニターがジョブを停止しています。 </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> 完了</span>:タスクモニタージョブに割り当てられたジョブが完了しました。 </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> 失敗</span>:致命的なエラーを示します。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

