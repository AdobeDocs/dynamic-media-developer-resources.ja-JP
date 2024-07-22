---
description: これらのサーバー設定を使用して、監視および警告システムを構成します。
solution: Experience Manager
title: 監視および警告システム
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 監視および警告システム{#monitoring-and-alerting-system}

これらのサーバー設定を使用して、監視および警告システムを構成します。

## AS::monitorAlertGenerator.enableGlobalAlerting - システムに警告を送信する {#section-612f8ea61794426ab205e22e5f665fa9}

を「true」に設定し、メール通知設定を設定することで、メール通知を有効にします。 `false` に設定すると、すべてのメールアラートがオフになります。これは、メンテナンスのためにサーバーをオフラインにする場合に役立ちます。 ブール値。

## AS::mailSender.host - SMTP ホスト {#section-151df07e7b44446581339bb7abeeba7a}

SMTP メールサーバーの IP アドレス。

## AS::mailSender.port- SMTP ポート {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP E メール サーバーのリスニング ポート。

## AS::monitorAlertGenerator.messageTo - メッセージの受信者 {#section-0017bbaa15434117a70900c3f1163960}

アラートの送信先となる 1 つ以上のメールアドレス。 セミコロンを区切り文字として使用します。

## AS::monitorAlertGenerator.messageFrom - メッセージ送信者 {#section-db320cba4ac2438ca1cfe6abce4aed87}

**[!UICONTROL 送信元]** メールフィールドで使用する必要があるメールアドレス。

## AS::monitorAlertGenerator.alertInterval – 監視間隔 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

監視システムは、アラート間隔の間にアラート状態を蓄積し、各間隔の終わりに全ての蓄積されたアラートを含むアラートメールを送信する。 ミリ秒、整数値、60000 以上。 通常は 5 分または 10 分に設定します。

## AS::monitorAlertGenerator.heapSpaceResetInterval - ヒープ領域のアラート間隔 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

ヒープ領域アラートが発生してから別のアラートが発行されるまでの最小時間。 インターバル時間（ミリ秒単位）。 0 以上の整数値。

## AS::monitorAlertGenerator.minTrafficForAlerts - アラートを有効にする最小トラフィック {#section-8b4db2d6f96642309ca35c49eb3ab230}

1 秒あたりのリクエスト数。 トラフィックがこのしきい値を下回った場合、応答時間は発生せず、エラーアラートも発生しません。 0 に設定すると、トラフィック量に関係なく、応答時間とエラーアラートが送信されます。 実際の値は 0 以上。
