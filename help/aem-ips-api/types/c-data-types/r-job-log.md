---
description: ジョブの実行後のジョブログ。
seo-description: ジョブの実行後のジョブログ。
seo-title: JobLog
solution: Experience Manager
title: JobLog
topic: Scene7 Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JobLog{#joblog}

ジョブの実行後のジョブログ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 会社の担当。 |
| ` *`jobHandle`*` | `xsd:string` | ジョブハンドル。 |
| ` *`jobName`*` | `xsd:string` | ジョブ名. |
| ` *`originalJobName`*` | `xsd:string` | ジョブに送信された元の名前 `submitJob`。 |
| ` *`submitUserEmail`*` | `xsd:string` | ジョブを送信したユーザーの電子メールアドレス。 |
| ` *`logType`*` | `xsd:string` | ジョブのログタイプの選択。 |
| ` *`jobSubType`*` | `xsd:string` | 追加のジョブ情報。 |
| ` *`startDate`*` | `xsd:dateTime` | ジョブの開始日、時刻、およびタイムゾーン。 |
| ` *`endDate`*` | `xsd:dateTime` | ジョブの終了日、時刻、およびタイムゾーン。 |
| ` *`説明`*` | `xsd:string` | で最初に指定されたジョブの説明 `submitJob`。 |
| ` *`fileSuccessCount`*` | `xsd:int` | 正常に処理されたファイルの数。 |
| ` *`fileErrorCount`*` | `xsd:int` | エラーの原因となったファイルの数。 |
| ` *`fileWarningCount`*` | `xsd:int` | 警告を生成したファイルの数。 |
| ` *`fileDuplicateCount`*` | `xsd:int` | 重複ファイルの数。 |
| ` *`fileUpdateCount`*` | `xsd:int` | 更新されたファイルの数。 |
| ` *`totalFileCount`*` | `xsd:int` | ログジョブで処理されたファイルの数。 |
| ` *`transferSuccessCount`*` | `xsd:int` | 成功した転送の数。 |
| ` *`transferErrorCount`*` | `xsd:int` | 転送エラーの数。 |
| ` *`transferWarningCount`*` | `xsd:int` | 転送の警告の数。 |
| ` *`fatalError`*` | `xsd:boolean` | ジョブが致命的なエラーを生成したかどうか。 |
| ` *`detailTotalRows`*` | `xsd:int` | クエリに一致する行の合計数。ページサイズの制限により、のサイズより大き `detailArray` い場合があります。 |
| ` *`detailArray`*` | `types:JobLogDetailArray` | ログに記録されたジョブの詳細の配列です。 |

