---
description: ジョブが実行された後のジョブ ログ。
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
TQID: 'https://experienceleague.adobe.com/R3h5NRNxH00Qskdzvw6ul55STF234SudJbjLGYrd238'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 187
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

ジョブが実行された後のジョブ ログ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| companyHandle | `xsd:string` | 会社のハンドル。 |
| jobHandle | `xsd:string` | ジョブハンドル： |
| jobName | `xsd:string` | ジョブ名： |
| originalJobName | `xsd:string` | ジョブの元の名前が`submitJob`で送信されました。 |
| submitUserEmail | `xsd:string` | ジョブを送信したユーザーの電子メールアドレス。 |
| logType | `xsd:string` | ジョブログタイプの選択。 |
| jobSubType | `xsd:string` | ジョブに関する追加情報。 |
| startDate | `xsd:dateTime` | ジョブの開始日、時刻、タイムゾーン。 |
| endDate | `xsd:dateTime` | ジョブの終了日、時刻、タイムゾーン。 |
| [!DNL description] | `xsd:string` | 最初に`submitJob`で指定されたジョブの説明。 |
| fileSuccessCount | `xsd:int` | 正常に処理されたファイルの数。 |
| fileErrorCount | `xsd:int` | エラーが発生したファイルの数。 |
| fileWarningCount | `xsd:int` | 警告を生成したファイルの数。 |
| fileDuplicateCount | `xsd:int` | 重複ファイルの数。 |
| fileUpdateCount | `xsd:int` | 更新されたファイル数。 |
| totalFileCount | `xsd:int` | ログに記録されたジョブによって処理されたファイルの数。 |
| transferSuccessCount | `xsd:int` | 成功した転送の数。 |
| transferErrorCount | `xsd:int` | 転送エラー数。 |
| transferWarningCount | `xsd:int` | 転送の警告の数。 |
| fatalError | `xsd:boolean` | ジョブで致命的なエラーが発生したかどうかを確認します。 |
| detailTotalRows | `xsd:int` | クエリに一致する行の合計数。ページサイズの制限により、`detailArray`のサイズよりも大きい可能性があります。 |
| detailArray | `types:JobLogDetailArray` | ログに記録されたジョブに関する詳細の配列。 |

