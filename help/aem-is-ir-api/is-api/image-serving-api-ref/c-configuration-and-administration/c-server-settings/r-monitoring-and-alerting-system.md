---
description: 監視および警告システムを構成するには、次のサーバー設定を使用します。
seo-description: 監視および警告システムを構成するには、次のサーバー設定を使用します。
seo-title: 監視と警告システム
solution: Experience Manager
title: 監視と警告システム
topic: Scene7 Image Serving - Image Rendering API
uuid: 944c7d53-09ec-443e-ac8c-85684d8fda0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 監視と警告システム{#monitoring-and-alerting-system}

監視および警告システムを構成するには、次のサーバー設定を使用します。

## AS::monitorAlertGenerator.enableGlobalAlerting — アラートシステムの有効化 {#section-612f8ea61794426ab205e22e5f665fa9}

「true」に設定し、電子メール通知を設定して、電子メール通知を有効にします。 すべての電子メ `false` ールアラートをオフにする設定です。この設定は、メンテナンスのためにサーバーをオフラインにする場合に便利です。 Boolean.

## AS::mailSender.host - SMTPホスト {#section-151df07e7b44446581339bb7abeeba7a}

SMTP電子メールサーバーのIPアドレス。

## AS::mailSender.port- SMTPポート {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP電子メールサーバーのリスニングポートです。

## AS::monitorAlertGenerator.messageTo — メッセージ受信者 {#section-0017bbaa15434117a70900c3f1163960}

アラートの送信先の1つ以上の電子メールアドレス。 セミコロンを区切り文字として使用します。

## AS::monitorAlertGenerator.messageFrom — メッセージの送信者 {#section-db320cba4ac2438ca1cfe6abce4aed87}

「送信者の電子メール」フィールドで使用する **[!UICONTROL 電子メール]** ・アドレス。

## AS::monitorAlertGenerator.alertInterval — 監視間隔 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

監視システムは、アラート間隔中にアラート条件を蓄積し、各間隔の終わりに蓄積されたすべてのアラートを含むアラート電子メールを送信します。 ミリ秒、60000以上の整数値。 通常は5 ～ 10分に設定します。

## AS::monitorAlertGenerator.heapSpaceResetInterval — ヒープ領域の警告の間隔 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

ヒープ領域の警告が発生してから別の警告が発生するまでの最小時間。 間隔（ミリ秒） 0以上の整数値。

## AS::monitorAlertGenerator.minTrafficForAlerts — アラートを有効にするための最小トラフィック {#section-8b4db2d6f96642309ca35c49eb3ab230}

1秒あたりのリクエスト数。 トラフィックがこのしきい値を下回った場合、応答時間およびエラーアラートは発生しません。 0に設定すると、トラフィック量に関係なく応答時間およびエラーアラートが送信されます。 0以上の実数です。
