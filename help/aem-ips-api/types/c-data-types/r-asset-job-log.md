---
description: 特定のアセットに関連付けられているジョブログエントリの詳細。 getAssetJobLogsによって返されるデータ。
seo-description: 特定のアセットに関連付けられているジョブログエントリの詳細。 getAssetJobLogsによって返されるデータ。
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Scene7 Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 5%

---


# AssetJobLog{#assetjoblog}

特定のアセットに関連付けられているジョブログエントリの詳細。 getAssetJobLogsによって返されるデータ。

構文

## パラメータ {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブ名. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">ジョブログ内のメッセージ。 <p><span class="codeph"> logMessageresponseフィールドは、authHeaderlocaleフィールドに基づいてローカラ</span>  <span class="codeph"> </span> イズされます。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ログエントリ内のジョブのタイプ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> ジョブを送信したユーザーの電子メール。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> ジョブの日付。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：JobLogDetailArray</span> </td> 
   <td colname="col3"> 各ジョブログの補助ジョブログメッセージの配列。 </td> 
  </tr> 
 </tbody> 
</table>

