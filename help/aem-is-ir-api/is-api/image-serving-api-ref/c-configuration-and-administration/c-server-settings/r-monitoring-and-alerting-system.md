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
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# システムの監視と警告{#monitoring-and-alerting-system}

監視および警告システムを構成するには、次のサーバー設定を使用します。

## AS::monitorAlertGenerator.enableGlobalAllerting - Alerting System Enable {#section-612f8ea61794426ab205e22e5f665fa9}

電子メール通知を有効にするには、「true」に設定し、電子メール通知を設定します。 `false`に設定すると、すべての電子メールアラートがオフになります。これは、サーバーをオフラインにしてメンテナンスを行う場合に役立ちます。 Boolean.

## AS::mailSender.host - SMTPホスト{#section-151df07e7b44446581339bb7abeeba7a}

SMTP電子メールサーバーのIPアドレスです。

## AS::mailSender.port- SMTPポート{#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP電子メールサーバーのリスニングポートです。

## AS::monitorAlertGenerator.messageTo — メッセージ受信者{#section-0017bbaa15434117a70900c3f1163960}

アラートの送信先の1つ以上の電子メールアドレス。 セミコロンを区切り文字として使用します。

## AS::monitorAlertGenerator.messageFrom — メッセージ送信者{#section-db320cba4ac2438ca1cfe6abce4aed87}

**[!UICONTROL From]**&#x200B;電子メールフィールドで使用する電子メールアドレス。

## AS::monitorAlertGenerator.alertInterval — 監視間隔{#section-99cb2e3380c1499e9d5aec3671ed73c7}

監視システムは、アラート間隔中にアラート条件を蓄積し、各間隔の終わりに蓄積されたすべてのアラートを含むアラート電子メールを送信します。 ミリ秒、整数値、60000以上。 通常は5 ～ 10分に設定します。

## AS::monitorAlertGenerator.heapSpaceResetInterval — ヒープスペースの警告間隔{#section-fd5a2bf04ed44fdcaef20f77084151a8}

ヒープ領域の警告が発生してから、別の警告が発行されるまでの最小時間。 間隔（ミリ秒） 0以上の整数値。

## AS::monitorAlertGenerator.minTrafficForAlerts — アラートを有効にするための最小トラフィック{#section-8b4db2d6f96642309ca35c49eb3ab230}

1秒あたりの要求数。 トラフィックがこのしきい値を下回る場合、応答時間およびエラーアラートは発行されません。 トラフィック量に関係なく応答時間およびエラーアラートを送信する場合は、0に設定します。 0以上の実数です。
