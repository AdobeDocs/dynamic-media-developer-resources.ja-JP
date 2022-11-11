---
description: ジョブの実行後のジョブログ。
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---

# [!DNL JobLog]{#joblog}

ジョブの実行後のジョブログ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| companyHandle | `xsd:string` | 会社の取り扱い。 |
| jobHandle | `xsd:string` | ジョブハンドル。 |
| jobName | `xsd:string` | ジョブ名. |
| originalJobName | `xsd:string` | でジョブに送信された元の名前 `submitJob`. |
| submitUserEmail | `xsd:string` | ジョブを送信したユーザーの電子メールアドレス。 |
| logType | `xsd:string` | ジョブのログタイプの選択。 |
| jobSubType | `xsd:string` | 追加のジョブ情報。 |
| startDate | `xsd:dateTime` | ジョブの開始日、時刻、およびタイムゾーン。 |
| endDate | `xsd:dateTime` | ジョブの終了日、時刻、およびタイムゾーン。 |
| [!DNL description] | `xsd:string` | 最初に指定されたジョブの説明 ( `submitJob`. |
| fileSuccessCount | `xsd:int` | 正常に処理されたファイル数。 |
| fileErrorCount | `xsd:int` | エラーの原因となったファイルの数。 |
| fileWarningCount | `xsd:int` | 警告を生成したファイルの数。 |
| fileDuplicateCount | `xsd:int` | 重複ファイルの数。 |
| fileUpdateCount | `xsd:int` | 更新されたファイルの数。 |
| totalFileCount | `xsd:int` | ログに記録されたジョブで処理されたファイルの数。 |
| transferSuccessCount | `xsd:int` | 成功した転送の数。 |
| transferErrorCount | `xsd:int` | 転送エラーの数。 |
| transferWarningCount | `xsd:int` | 転送の警告数。 |
| fatalError | `xsd:boolean` | ジョブで致命的なエラーが発生したかどうか。 |
| detailTotalRows | `xsd:int` | クエリに一致する行の合計数 ( `detailArray` ページサイズの制限によります。 |
| detailArray | `types:JobLogDetailArray` | ログに記録されたジョブに関する詳細の配列。 |
