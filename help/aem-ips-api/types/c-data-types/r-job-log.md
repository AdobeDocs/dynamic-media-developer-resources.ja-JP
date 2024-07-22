---
description: ジョブが実行された後のジョブ ログ。
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

ジョブが実行された後のジョブ ログ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| companyHandle | `xsd:string` | 会社ハンドル。 |
| jobHandle | `xsd:string` | ジョブハンドル。 |
| jobName | `xsd:string` | ジョブ名。 |
| originalJobName | `xsd:string` | `submitJob` を含むジョブに対して送信された元の名前。 |
| submitUserEmail | `xsd:string` | ジョブを送信したユーザーのメールアドレス。 |
| logType | `xsd:string` | ジョブ ログの種類を選択します。 |
| jobSubType | `xsd:string` | 追加のジョブ情報。 |
| startDate | `xsd:dateTime` | ジョブの開始日、時刻、およびタイムゾーン。 |
| endDate | `xsd:dateTime` | ジョブの終了日、時刻、およびタイムゾーン。 |
| [!DNL description] | `xsd:string` | `submitJob` で最初に指定されたジョブの説明。 |
| fileSuccessCount | `xsd:int` | 正常に処理されたファイルの数。 |
| fileErrorCount | `xsd:int` | エラーの原因となったファイルの数。 |
| fileWarningCount | `xsd:int` | 警告が生成されたファイルの数。 |
| fileDuplicateCount | `xsd:int` | 重複ファイルの数。 |
| fileUpdateCount | `xsd:int` | 更新されたファイルの数。 |
| totalFileCount | `xsd:int` | ログに記録されたジョブによって処理されたファイルの数。 |
| transferSuccessCount | `xsd:int` | 成功した転送の数。 |
| transferErrorCount | `xsd:int` | 転送エラーの数。 |
| transferWarningCount | `xsd:int` | 転送警告の数。 |
| fatalError | `xsd:boolean` | ジョブが致命的なエラーを生成したかどうか。 |
| detailTotalRows | `xsd:int` | クエリに一致する行の合計数。ページサイズの制限により、`detailArray` のサイズを超える場合があります。 |
| detailArray | `types:JobLogDetailArray` | 記録されたジョブに関する詳細の配列。 |
