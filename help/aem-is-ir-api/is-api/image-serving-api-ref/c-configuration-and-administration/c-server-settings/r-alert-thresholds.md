---
description: これらのサーバー設定を使用して、アラートのしきい値を構成します。
solution: Experience Manager
title: アラートしきい値
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# アラートしきい値{#alert-thresholds}

これらのサーバー設定を使用して、アラートのしきい値を構成します。

## AS:: monitorAlertGenerator.maxAverageResponseTime – 応答時間しきい値 AS:: monitorAlertGenerator.maxAverageResponseTime – 応答時間 {#section-35111039ac6c4a63ba23fc2c828ab726}

サンプリング間隔中に要求を処理する平均時間がここで設定したしきい値を超えると、応答時間アラートが生成されます。 ミリ秒単位で表します。0 以上の整数です。 一般的な値は、操作の複雑さに応じて 100 ～ 1000 ミリ秒です。

>[!NOTE]
>
>4xx または 5xx の応答ステータスになるリクエストは、このアラートでは考慮されません。

## AS::monitorAlertGenerator.maxErrorRate - エラー応答率のしきい値 AS::monitorAlertGenerator.maxErrorRate - エラー応答率 {#section-76ba77fd3102419395e0f86719a1f3ec}

サンプリング間隔中の合計応答に対する HTTP エラー応答の割合が指定のしきい値を超えると、エラー・アラートが発行されます。

0.0 ～ 1.0 の間の実際の値。通常は 0.005 ～ 0.1 に設定します。1 に設定すると、エラーアラートが無効になります。

## AS::monitorAlertGenerator.minRequestRate – 低トラフィックのしきい値 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

最小トラフィックアラートは、現在のサンプリング間隔中に受信した 1 秒あたりの平均要求数がこの閾値を下回った場合に送信されます。 この値を 0 に設定して、アラートを無効にします。 1 秒あたりのリクエスト数で表されます。 実際の値は 0 以上。

## AS::monitorAlertGenerator.minFreeHeapSpace – 空きヒープ領域のしきい値 {#section-ce6705045f6842769030ccb1894594cc}

Java の空きヒープ領域の最小値を指定します。 優先度アラートは、空きヒープ領域がこのしきい値を下回っている場合、Java ガベージコレクションサイクルの直後に送信されます。 [!DNL Platform Server] の安全な操作には 50 MB をお勧めします。 空きヒープ領域をこの値の上に維持すると、ガベージコレクションサイクルの頻度が減り、サーバー全体のパフォーマンスが向上する可能性があります。 バイト単位の 0 以上の整数値。

## AS::monitorAlertGenerator.maxOverlap – 同時要求の最大数 {#section-ddc6925bff944758ab19bcc9cf3f2589}

重複アラートは、平均化間隔の間に同時に処理されたリクエストの平均数がこのしきい値を超えた場合にトリガーされます。 重複が大きい場合は、サーバー過負荷状態の可能性を示している可能性があります。

1 以上の整数値 一般的な範囲は 20 ～ 50 で、キャッシュのヒット率とリクエストの複雑さに応じて異なります。

## AS::monitorAlertGenerator.lockedThreshold - ロックされた要求のしきい値 {#section-012a1c9937d445708380339279c62d80}

リクエストがロック済みまたはハング済みと見なされるまでに、リクエストを保留にする秒数を指定します。 ロック済み要求アラートは、平均化間隔の終わりに、少なくとも 1 つの要求が指定された期間より長い期間保留されている場合に発行されます。 ミリ秒単位の正の整数値。

外部の HTTP サーバーからデータを取得する必要がある複雑なレンダリング要求やリクエストを考慮するには、この値を 30 秒以上に設定することをお勧めします（このような条件がこのアラートで検出されない限り）。
