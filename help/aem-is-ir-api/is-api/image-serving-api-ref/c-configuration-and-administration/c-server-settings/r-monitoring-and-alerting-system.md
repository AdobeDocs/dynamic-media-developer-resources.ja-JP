---
description: これらのサーバー設定を使用して、監視およびアラートシステムを設定します。
solution: Experience Manager
title: 監視およびアラートシステム
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
TQID: 'https://experienceleague.adobe.com/n8Xw2xwdJNYlTVQusHBqP0aEpMYyPuE135TR30FLZKQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 240
ht-degree: 0%

---

# 監視およびアラートシステム{#monitoring-and-alerting-system}

これらのサーバー設定を使用して、監視およびアラートシステムを設定します。

## AS::monitorAlertGenerator.enableGlobalAlerting - Alerting System Enable {#section-612f8ea61794426ab205e22e5f665fa9}

「true」に設定し、メール通知設定を設定して、メール通知を有効にします。 `false`に設定すると、すべての電子メールアラートがオフになります。これは、サーバーをメンテナンスのためにオフラインにする場合に便利です。 ブーリアン。

## AS::mailSender.host - SMTP ホスト {#section-151df07e7b44446581339bb7abeeba7a}

SMTP メールサーバーのIP アドレス。

## AS::mailSender.port- SMTP ポート {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP メールサーバーのリッスン ポート。

## AS::monitorAlertGenerator.messageTo - メッセージ受信者 {#section-0017bbaa15434117a70900c3f1163960}

アラートを送信する1つ以上のメールアドレス。 セミコロンを区切り記号として使用します。

## AS::monitorAlertGenerator.messageFrom - Message Sender {#section-db320cba4ac2438ca1cfe6abce4aed87}

**[!UICONTROL 送信元]**&#x200B;電子メールフィールドで使用する電子メールアドレス。

## AS::monitorAlertGenerator.alertInterval - Monitoring Interval {#section-99cb2e3380c1499e9d5aec3671ed73c7}

監視システムは、アラート間隔の間にアラート条件を蓄積し、各間隔の終わりにすべての蓄積されたアラートを含むアラートメールを送信します。 ミリ秒、整数値、60000以上。 通常、5分または10分に設定します。

## AS::monitorAlertGenerator.heapSpaceResetInterval - ヒープ スペース アラート間隔 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

ヒープスペースアラートが発行されるまでの最小時間。 インターバル時間（ミリ秒）。 0以上の整数値。

## AS::monitorAlertGenerator.minTrafficForAlerts - アラートを有効にする最小トラフィック {#section-8b4db2d6f96642309ca35c49eb3ab230}

リクエスト数/秒。 トラフィックがこの閾値を下回った場合、応答時間とエラーアラートは発生しません。 0に設定すると、トラフィック量に関係なく、応答時間とエラーアラートが送信されます。 実数値0以上。
