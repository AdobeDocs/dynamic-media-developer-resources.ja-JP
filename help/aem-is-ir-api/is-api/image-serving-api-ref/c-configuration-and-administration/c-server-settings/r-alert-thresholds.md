---
description: これらのサーバー設定を使用して、アラートしきい値を設定します。
solution: Experience Manager
title: アラートしきい値
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
TQID: 'https://experienceleague.adobe.com/mu--4-idJqrtGhbeVu3GP3LxJ4ZRL6zn1XZxTH7DLw4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 410
ht-degree: 0%

---

# アラートしきい値{#alert-thresholds}

これらのサーバー設定を使用して、アラートしきい値を設定します。

## AS:: monitorAlertGenerator.maxAverageResponseTime – 応答時間しきい値AS: monitorAlertGenerator.maxAverageResponseTime – 応答時間 {#section-35111039ac6c4a63ba23fc2c828ab726}

レスポンス時間アラートは、サンプリング間隔におけるリクエストを処理する平均時間がここで設定されたしきい値を超えたときに発行されます。 0以上の整数をミリ秒単位で表します。 典型的な値は、操作の複雑さに応じて100 ～ 1000 msecです。

>[!NOTE]
>
>4xxまたは5xxの応答ステータスになるリクエストは、このアラートでは考慮されません。

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate ThresholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

エラーアラートは、サンプリング間隔における合計応答に対するHTTP エラー応答の比率が、指定されたしきい値を超えた場合に発行されます。

0.0 ～ 1.0の実数値。通常は0.005 ～ 0.1の範囲に設定します。 エラーアラートを無効にするには、1に設定します。

## AS::monitorAlertGenerator.minRequestRate - Low Traffic Threshold {#section-8dfb89ed138640fd86f5ce1dae2a533e}

現在のサンプリング間隔で受信される1秒あたりのリクエストの平均数がこの閾値を下回ると、最小トラフィックアラートが送信されます。 この値を0に設定して、アラートを無効にします。 1秒あたりのリクエスト数で表されます。 実数値0以上。

## AS::monitorAlertGenerator.minFreeHeapSpace – 空きヒープスペースのしきい値 {#section-ce6705045f6842769030ccb1894594cc}

空きJava ヒープ領域の最小値を指定します。 優先度アラートは、空きヒープスペースがこの閾値を下回る場合に、Java ガベージコレクションサイクルの直後に送信されます。 [!DNL Platform Server]を安全に操作するには、50 MBをお勧めします。 空きヒープ領域をこの値より大きくすると、ガベージコレクションサイクルの頻度が減少し、サーバー全体のパフォーマンスが向上する可能性があります。 0以上のバイト単位の整数値。

## AS::monitorAlertGenerator.maxOverlap – 同時リクエストの最大数 {#section-ddc6925bff944758ab19bcc9cf3f2589}

平均化間隔で同時に処理されたリクエストの平均数がこの閾値を超えると、重複アラートがトリガーされます。 重複が多い場合は、サーバーのオーバーロード状態が発生している可能性があります。

整数値1以上。 一般的な範囲は、キャッシュヒット率とリクエストの複雑さによって異なり、20 ～ 50です。

## AS::monitorAlertGenerator.lockedThreshold - Locked Request Threshold {#section-012a1c9937d445708380339279c62d80}

リクエストがロックまたはハングされたとみなされるまでに保留にする必要がある秒数を指定します。 平均化期間の終了時に、少なくとも1つのリクエストが指定された期間を超えて保留中である場合、ロック済みリクエストアラートが発行されます。 正の整数値（ミリ秒）。

外部HTTP サーバーからデータを取得する複雑なレンダリング要求と要求を考慮するには、この値を30秒以上に設定することをお勧めします（このアラートでそのような条件が検出される場合を除く）。
