---
description: これらのサーバー設定を使用して、監視および警告システムを構成します。
solution: Experience Manager
title: 監視および警告システム
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# 監視および警告システム{#monitoring-and-alerting-system}

これらのサーバー設定を使用して、監視および警告システムを構成します。

## AS::monitorAlertGenerator.enableGlobalAlerting — アラートシステムの有効化 {#section-612f8ea61794426ab205e22e5f665fa9}

を「true」に設定し、電子メール通知を設定することで、電子メール通知を有効にします。 `false`に設定すると、すべての電子メールアラートがオフになります。これは、メンテナンスのためにサーバーをオフラインにする場合に役立ちます。 Boolean.

## AS::mailSender.host - SMTPホスト {#section-151df07e7b44446581339bb7abeeba7a}

SMTP電子メールサーバーのIPアドレス。

## AS::mailSender.port- SMTPポート {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP電子メールサーバーのリスニングポートです。

## AS::monitorAlertGenerator.messageTo — メッセージ受信者 {#section-0017bbaa15434117a70900c3f1163960}

アラートの送信先となる1つ以上の電子メールアドレス。 セミコロンを区切り文字として使用します。

## AS::monitorAlertGenerator.messageFrom — メッセージ送信者 {#section-db320cba4ac2438ca1cfe6abce4aed87}

**[!UICONTROL From]** emailフィールドで使用する電子メールアドレス。

## AS::monitorAlertGenerator.alertInterval — 監視間隔 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

監視システムは、アラート間隔中にアラート条件を蓄積し、各間隔の最後に蓄積されたすべてのアラートを含むアラート電子メールを送信します。 ミリ秒、整数値、60000以上。 通常は5 ～ 10分に設定します。

## AS::monitorAlertGenerator.heapSpaceResetInterval — ヒープスペースのアラート間隔 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

ヒープスペースアラートが発生してから、別のヒープスペースアラートが発生するまでの最小時間。 間隔時間（ミリ秒）。 0以上の整数値。

## AS::monitorAlertGenerator.minTrafficForAlerts — アラートを有効にする最小トラフィック {#section-8b4db2d6f96642309ca35c49eb3ab230}

1秒あたりの要求数。 トラフィックがこのしきい値を下回る場合、応答時間およびエラーアラートは発生しません。 トラフィック量に関係なく応答時間およびエラーアラートを送信するには、0に設定します。 0以上の実数。
