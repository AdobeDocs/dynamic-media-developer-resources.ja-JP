---
description: これらのサーバー設定を使用して、アラートのしきい値を構成します。
solution: Experience Manager
title: アラートしきい値
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# アラートしきい値{#alert-thresholds}

これらのサーバー設定を使用して、アラートのしきい値を構成します。

## AS::monitorAlertGenerator.maxAverageResponseTime — 応答時間のしきい値 AS::monitorAlertGenerator.maxAverageResponseTime — 応答時間 {#section-35111039ac6c4a63ba23fc2c828ab726}

応答時間アラートは、サンプリング間隔中のリクエストの処理平均時間がここで設定したしきい値を超えると発生します。 ミリ秒単位で表現0 以上の整数。 操作の複雑さに応じて、一般的な値は 100 ～ 1000 ミリ秒です。

>[!NOTE]
>
>このアラートでは、応答ステータスが 4xx または 5xx になるリクエストは考慮されません。

## AS::monitorAlertGenerator.maxErrorRate — エラー応答率しきい値 AS::monitorAlertGenerator.maxErrorRate — エラー応答率 {#section-76ba77fd3102419395e0f86719a1f3ec}

エラーアラートは、サンプリング間隔中の合計応答に対する HTTP エラー応答の比率が、指定されたしきい値を超えた場合に発生します。

0.0 ～ 1.0 の実数値。通常は 0.005 ～ 0.1 に設定します。エラーアラートを無効にするには、1 に設定します。

## AS::monitorAlertGenerator.minRequestRate — 低トラフィックしきい値 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

最小トラフィックアラートは、現在のサンプリング間隔で受信した 1 秒あたりの平均リクエスト数がこのしきい値を下回った場合に送信されます。 この値を 0 に設定して、アラートを無効にします。 1 秒あたりのリクエスト数で表されます。 0 以上の実数。

## AS::monitorAlertGenerator.minFreeHeapSpace — 空きヒープ領域のしきい値 {#section-ce6705045f6842769030ccb1894594cc}

最小の空き Java ヒープ領域を指定します。 空きヒープ領域がこのしきい値を下回ると、Java のガベージコレクションサイクルの直後に優先度アラートが送信されます。 安全な操作のために、50 MB が推奨されます [!DNL Platform Server]. この値より大きい空きヒープ領域を保持すると、ガベージコレクションサイクルの頻度が減り、サーバー全体のパフォーマンスが向上する可能性があります。 0 以上の整数値（バイト単位）。

## AS::monitorAlertGenerator.maxOverlap — 同時要求の最大数 {#section-ddc6925bff944758ab19bcc9cf3f2589}

重複アラートは、平均化間隔中に同時に処理されたリクエストの平均数がこのしきい値を超えた場合にトリガーされます。 重複が多い場合は、サーバーの過負荷状態が発生する可能性があります。

1 以上の整数値。 一般的な範囲は、キャッシュのヒット率とリクエストの互換性に応じて、20～50 です。

## AS::monitorAlertGenerator.lockedThreshold — ロックされたリクエストのしきい値 {#section-012a1c9937d445708380339279c62d80}

リクエストがロックまたはハングしたと見なされるまでの保留中の秒数を指定します。 平均化間隔の終了時に、少なくとも 1 つのリクエストが指定された期間より長く保留中の場合、ロックされたリクエストアラートが発行されます。 正の整数値（ミリ秒）。

外部 HTTP サーバーからのデータの取得に関連する複雑なレンダリング要求や要求を考慮するには、この値を 30 秒以上に設定することをお勧めします（このアラートで条件が検出される場合を除く）。
