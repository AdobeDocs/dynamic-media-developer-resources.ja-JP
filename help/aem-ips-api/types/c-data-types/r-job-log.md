---
description: ジョブの実行後のジョブログ。
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---


# JobLog{#joblog}

ジョブの実行後のジョブログ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 会社ハンドル |
| `*`jobHandle`*` | `xsd:string` | ジョブハンドル。 |
| `*`jobName`*` | `xsd:string` | ジョブ名. |
| `*`originalJobName`*` | `xsd:string` | `submitJob`を持つジョブに対して送信された元の名前。 |
| `*`submitUserEmail`*` | `xsd:string` | ジョブを送信したユーザーの電子メールアドレス。 |
| `*`logType`*` | `xsd:string` | ジョブログタイプの選択。 |
| `*`jobSubType`*` | `xsd:string` | 追加のジョブ情報。 |
| `*`startDate`*` | `xsd:dateTime` | ジョブの開始日、時刻およびタイムゾーン。 |
| `*`endDate`*` | `xsd:dateTime` | ジョブの終了日、時刻およびタイムゾーン。 |
| `*`description`*` | `xsd:string` | `submitJob`で最初に指定されたジョブの説明。 |
| `*`fileSuccessCount`*` | `xsd:int` | 正常に処理されたファイルの数。 |
| `*`fileErrorCount`*` | `xsd:int` | エラーの原因となったファイルの数。 |
| `*`fileWarningCount`*` | `xsd:int` | 警告を生成したファイルの数。 |
| `*`fileDuplicateCount`*` | `xsd:int` | 重複ファイルの数。 |
| `*`fileUpdateCount`*` | `xsd:int` | 更新されたファイルの数。 |
| `*`totalFileCount`*` | `xsd:int` | ログジョブで処理されたファイルの数。 |
| `*`transferSuccessCount`*` | `xsd:int` | 成功した転送の数。 |
| `*`transferErrorCount`*` | `xsd:int` | 転送エラーの数。 |
| `*`transferWarningCount`*` | `xsd:int` | 転送の警告の数。 |
| `*`fatalError`*` | `xsd:boolean` | ジョブが致命的なエラーを生成したかどうか。 |
| `*`detailTotalRows`*` | `xsd:int` | クエリに一致する行の合計数です。ページサイズの制限により、`detailArray`のサイズよりも大きい場合があります。 |
| `*`detailArray`*` | `types:JobLogDetailArray` | ログに記録されたジョブに関する詳細の配列です。 |

