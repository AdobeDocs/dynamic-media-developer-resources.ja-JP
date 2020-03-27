---
description: これらのサーバー設定を使用して、アラートのしきい値を設定します。
seo-description: これらのサーバー設定を使用して、アラートのしきい値を設定します。
seo-title: アラートしきい値
solution: Experience Manager
title: アラートしきい値
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# アラートしきい値{#alert-thresholds}

これらのサーバー設定を使用して、アラートのしきい値を設定します。

## AS:monitorAlertGenerator.maxAverageResponseTime — 応答時間のしきい値：monitorAlertGenerator.maxAverageResponseTime — 応答時間 {#section-35111039ac6c4a63ba23fc2c828ab726}

応答時間アラートは、サンプリング間隔中の要求を処理する平均時間が、ここで設定したしきい値を超えた場合に発生します。 ミリ秒単位で表します。0以上の整数。 一般的な値は、操作の複雑さに応じて100 ～ 1000ミリ秒です。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>4xxまたは5xxの応答ステータスになるリクエストは、このアラートに対しては考慮されません。

## AS::monitorAlertGenerator.maxErrorRate — エラー応答率しきい値AS::monitorAlertGenerator.maxErrorRate — エラー応答率 {#section-76ba77fd3102419395e0f86719a1f3ec}

サンプリング間隔中の合計応答に対するHTTPエラー応答の比率が、指定したしきい値を超えると、エラーアラートが発行されます。

0.0 ～ 1.0の実数です。通常、0.005 ～ 0.1に設定します。1に設定すると、エラー警告が無効になります。

## AS::monitorAlertGenerator.minRequestRate — 低トラフィックしきい値 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

最小トラフィックアラートは、現在のサンプリング間隔中に受信した1秒あたりの平均リクエスト数がこのしきい値を下回った場合に送信されます。 この値を0に設定して、アラートを無効にします。 リクエスト/秒で表されます。 0以上の実数です。

## AS::monitorAlertGenerator.minFreeHeapSpace — 空きヒープ領域のしきい値 {#section-ce6705045f6842769030ccb1894594cc}

Javaの最小空きヒープ領域を指定します。 優先度アラートは、空きヒープ領域がこのしきい値を下回る場合、Javaのガベージコレクションサイクルの直後に送信されます。 プラットフォームサーバーを安全に動作させるために、50 MBをお勧めします。 この値を超える空きヒープ領域を保持すると、ガベージコレクションサイクルの頻度が減り、サーバー全体のパフォーマンスが向上する可能性があります。 0以上のバイト単位の整数値。

## AS::monitorAlertGenerator.maxOverlap — 同時リクエストの最大数 {#section-ddc6925bff944758ab19bcc9cf3f2589}

重複アラートは、平均間隔中に同時に処理されたリクエストの平均数がこのしきい値を超えた場合にトリガーされます。 重複が多い場合は、サーバの過負荷状態が発生する可能性があります。

1以上の整数値。 通常の範囲は、キャッシュのヒット率とリクエストの複雑さに応じて、20 ～ 50です。

## AS::monitorAlertGenerator.lockedThreshold — ロックされた要求のしきい値 {#section-012a1c9937d445708380339279c62d80}

要求がロックまたはハングしたと見なされるまでに保留される必要がある秒数を指定します。 平均化間隔の終わりに、少なくとも1つのリクエストが指定した期間を超えて保留中の場合は、ロックされたリクエストのアラートが発行されます。 正の整数値（ミリ秒）。

外部HTTPサーバーからのデータの取得を伴う複雑なレンダリング要求や要求を考慮するには、この値を30秒以上に設定することをお勧めします（このアラートでそのような条件が検出される場合を除く）。
