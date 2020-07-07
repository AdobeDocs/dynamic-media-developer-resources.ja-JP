---
description: トレースログをデバッグするには、次のサーバー設定を使用します。
seo-description: トレースログをデバッグするには、次のサーバー設定を使用します。
seo-title: Debug_traceログ
solution: Experience Manager
title: Debug_traceログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Debug_traceログ{#debug-trace-logging}

トレースログをデバッグするには、次のサーバー設定を使用します。

>[!NOTE]
>
>すべてのログファイルをと同じフォルダーに書き込むように設定することをお勧めし `TC::directory`ます。 これにより、すべての画像サービングのログファイルがで設定されたログファイルの自動ローテーションに関与するようにな `TC::maxDays`り、ディスク領域不足によるサーバの不安定性を防ぐことができます。

## SV::log — サーバスーパーバイザトレースログファイルのパス {#section-3697bc480ff646e79cacc2812c55ef26}

サーバースーパーバイザログファイルのフォルダ名とベースファイル名。 パスは、絶対パスまたは相対パスにすることができ *[!DNL install_folder]*&#x200B;ます。 サーバスーパーバイザは、ファイル名にハイフンと現在の日付( *[!DNL -yyyy-mm-dd]*)を追加します（ファイルのサフィックスがある場合はその前）。 Platformサーバー( `PS::LogFolder`)が実装するログファイル管理を活用するため、すべてのログファイルをPlatformサーバーのログファイル( `PS::LogDays`)と同じフォルダーに送ることをお勧めします。 初期設定は [!DNL logs/Supervisor.log].

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 サーバスーパーバイザが必要な作成、読み取り、書き込みの権限を持つように、アクセス権限が設定されていることを確認します。

## SV::tracelevel — サーバスーパーバイザトレースログレベル {#section-36f8634741da4c618d67aa628b5fe474}

ログレベルは、1、2、3または4です。 初期設定は 2 です

## IS::Log - Image Serverデバッグログファイルのパス {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Serverトレースログファイルのフォルダーとベースファイル名 パスは、絶対パスまたは相対パスにすることができ *[!DNL install_folder]*&#x200B;ます。 ImageServerは、ファイル名にハイフンと現在の日付( *[!DNL -yyyy-mm-dd]*)を付加します（ファイル名の前にある場合はファイルのサフィックスの前）。 Image Serverのログファイルは、Image Serverのログファイルと同じPlatformー( `PS::LogFolder`)に送信して、Platformサーバーが実装するログファイル管理を活用することをお勧めします( `PS::LogDays`を参照)。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 画像サービングに必要な作成、読み取りおよび書き込み権限が与えられるように、アクセス権限が設定されていることを確認します。

## IS:TraceClient - Image Serverのデバッグログレベル {#section-3851f1f68e404430985c629ac80534db}

ログレベルは1、2、3または4に設定できます（デフォルトは2）。

レベル1では、開始のアップ、シャットダウン、Platformサーバーの接続に関連するイベントが記録されます。

レベル2では、ソースイメージへの接続と切断もログに記録されます。

レベル3では、ピクセルデータの要求のログと同じ配信がPlatformサーバに追加されます。

レベル4では、Platformサーバーから受信したすべてのメッセージが記録されます。

ログファイルが非常に大きくなる可能性があるので、レベル3とレベル4はデバッグ目的でのみ使用してください。

## IS::TraceStatsInterval - Image Server統計ログの間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Serverは、この設定で指定された間隔で、メモリ統計をトレースログファイルに書き込みます。 有効な範囲は5 ～ 86,400秒です。
