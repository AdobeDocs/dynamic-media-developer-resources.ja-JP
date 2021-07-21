---
description: これらのサーバー設定を使用して、アラートのしきい値を構成します。
solution: Experience Manager
title: アラートのしきい値
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# アラートのしきい値{#alert-thresholds}

これらのサーバー設定を使用して、アラートのしきい値を構成します。

## AS::monitorAlertGenerator.maxAverageResponseTime — 応答時間のしきい値：monitorAlertGenerator.maxAverageResponseTime — 応答時間 {#section-35111039ac6c4a63ba23fc2c828ab726}

応答時間アラートは、サンプリング間隔中に要求を処理する平均時間がここで設定したしきい値を超えた場合に発生します。 ミリ秒単位で表現されます。0以上の整数。 操作の複雑さに応じて、一般的な値は100 ～ 1000ミリ秒です。

>[!NOTE]
>
>4xxまたは5xxの応答ステータスになるリクエストは、このアラートでは考慮されません。

## AS::monitorAlertGenerator.maxErrorRate — エラー応答率しきい値AS::monitorAlertGenerator.maxErrorRate — エラー応答率 {#section-76ba77fd3102419395e0f86719a1f3ec}

エラーアラートは、サンプリング間隔中の合計応答に対するHTTPエラー応答の割合が、指定されたしきい値を超えた場合に発行されます。

0.0 ～ 1.0の実数値。通常は0.005 ～ 0.1に設定します。エラーアラートを無効にするには、1に設定します。

## AS::monitorAlertGenerator.minRequestRate — 低トラフィックのしきい値 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

最小トラフィックアラートは、現在のサンプリング間隔中に受信した1秒あたりの平均リクエスト数がこのしきい値を下回った場合に送信されます。 この値を0に設定してアラートを無効にします。 リクエスト数/秒で表されます。 0以上の実数。

## AS::monitorAlertGenerator.minFreeHeapSpace — 空きヒープ領域のしきい値 {#section-ce6705045f6842769030ccb1894594cc}

最小空きJavaヒープ領域を指定します。 空きヒープ領域がこのしきい値を下回ると、Javaのガベージコレクションサイクルの直後に優先度アラートが送信されます。 Platform Serverを安全に動作させるには、50 MBをお勧めします。 この値を超える空きヒープ領域を維持すると、ガベージコレクションサイクルの頻度が減り、サーバー全体のパフォーマンスが向上する可能性があります。 0以上の整数値（バイト単位）。

## AS::monitorAlertGenerator.maxOverlap — 同時要求の最大数 {#section-ddc6925bff944758ab19bcc9cf3f2589}

重複アラートは、平均間隔中に同時に処理されたリクエストの平均数がこのしきい値を超えた場合にトリガーされます。 重複が多い場合は、サーバー過負荷状態が発生する可能性があります。

1以上の整数です。 一般的な範囲は、キャッシュヒット率とリクエストの互換性に応じて、20～50です。

## AS::monitorAlertGenerator.lockedThreshold — ロックされたリクエストのしきい値 {#section-012a1c9937d445708380339279c62d80}

要求がロックまたはハングしたと見なされるまでに保留中である必要がある秒数を指定します。 ロックされたリクエストのアラートは、平均間隔の終わりに、少なくとも1つのリクエストが指定された期間より長く保留中の場合に発行されます。 正の整数値（ミリ秒）。

外部HTTPサーバーからのデータの取得に関連する複雑なレンダリング要求や要求を考慮するには、この値を30秒以上に設定することをお勧めします（このアラートでそのような条件が検出される場合を除く）。
