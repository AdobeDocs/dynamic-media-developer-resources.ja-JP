---
description: これらのサーバー設定を使用して、アラートしきい値を設定します。
seo-description: これらのサーバー設定を使用して、アラートしきい値を設定します。
seo-title: アラートしきい値
solution: Experience Manager
title: アラートしきい値
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# アラートしきい値{#alert-thresholds}

これらのサーバー設定を使用して、アラートしきい値を設定します。

## AS::monitorAlertGenerator.maxAverageResponseTime — 応答時間のしきい値AS:monitorAlertGenerator.maxAverageResponseTime — 応答時間{#section-35111039ac6c4a63ba23fc2c828ab726}

応答時間アラートは、サンプリング間隔中の要求を処理する平均時間が、ここで設定したしきい値を超えた場合に発生します。 ミリ秒で表されます。0以上の整数。 一般的な値は、操作の複雑さに応じて、100 ～ 1000ミリ秒です。

>[!NOTE]
>
>4xxまたは5xxの応答ステータスになるリクエストは、このアラートでは考慮されません。

## AS::monitorAlertGenerator.maxErrorRate — エラー応答率のしきい値AS::monitorAlertGenerator.maxErrorRate — エラー応答率{#section-76ba77fd3102419395e0f86719a1f3ec}

エラーアラートは、サンプリング間隔中の合計応答に対するHTTPエラー応答の比率が、指定したしきい値を超えた場合に発行されます。

0.0 ～ 1.0の実数値。通常は0.005 ～ 0.1に設定します。エラー通知を無効にするには、1に設定します。

## AS::monitorAlertGenerator.minRequestRate — 低トラフィックのしきい値{#section-8dfb89ed138640fd86f5ce1dae2a533e}

最小トラフィックアラートは、現在のサンプリング間隔中に受信した1秒あたりの平均リクエスト数が、このしきい値を下回った場合に送信されます。 この値を0に設定して、アラートを無効にします。 1秒あたりの要求数で表されます。 0以上の実数です。

## AS::monitorAlertGenerator.minFreeHeapSpace — 空きヒープ領域のしきい値{#section-ce6705045f6842769030ccb1894594cc}

最小の空き領域のJavaヒープ領域を指定します。 空きヒープ領域がこのしきい値を下回ると、Javaのガベージコレクションサイクルの直後に優先度アラートが送信されます。 プラットフォームサーバーを安全に動作させるために、50 MBをお勧めします。 この値を超える空きヒープ領域を確保すると、ガベージコレクションサイクルの頻度が減り、サーバー全体のパフォーマンスが向上する可能性があります。 バイト単位の整数値（0以上）。

## AS::monitorAlertGenerator.maxOverlap — 同時要求の最大数{#section-ddc6925bff944758ab19bcc9cf3f2589}

重複アラートは、平均間隔中に同時に処理されたリクエストの平均数がこのしきい値を超えた場合にトリガーされます。 重複が大きい場合は、サーバの過負荷状態が発生する可能性があります。

1以上の整数です。 一般的な範囲は、キャッシュのヒット率とリクエストの互換性に応じて、20 ～ 50です。

## AS::monitorAlertGenerator.lockedThreshold — ロックされた要求のしきい値{#section-012a1c9937d445708380339279c62d80}

要求がロックまたはハングしたと見なされるまでに保留する必要がある秒数を指定します。 平均化間隔の終了時に、少なくとも1つのリクエストが指定した期間より長く保留中の場合は、ロックリクエストアラートが発行されます。 正の整数値（ミリ秒）。

外部のHTTPサーバーからのデータ取得に関連する複雑なレンダリング要求や要求を考慮するには、この値を30秒以上に設定することをお勧めします（このアラートでそのような条件が検出される場合を除く）。
