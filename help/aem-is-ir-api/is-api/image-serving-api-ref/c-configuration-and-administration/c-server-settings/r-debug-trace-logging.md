---
description: これらのサーバー設定を使用して、トレースログをデバッグします。
solution: Experience Manager
title: Debug_traceログ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Debug_traceログ{#debug-trace-logging}

これらのサーバー設定を使用して、トレースログをデバッグします。

>[!NOTE]
>
>`TC::directory`と同じフォルダーに書き込むすべてのログファイルを設定することをお勧めします。 これにより、すべての画像サービングログファイルが`TC::maxDays`で自動設定されたログファイルのローテーションに関与するようになり、ディスク領域不足によるサーバの不安定性を防ぐことができます。

## SV::log — サーバスーパーバイザトレースログファイルのパス {#section-3697bc480ff646e79cacc2812c55ef26}

サーバースーパーバイザログファイルのフォルダとベースファイル名。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスで指定できます。 サーバスーパーバイザは、ファイル名（ファイルサフィックスの前）にハイフンと現在の日付(*[!DNL -yyyy-mm-dd]*)を追加します。 Platform Server(`PS::LogDays`)で実装されたログファイル管理を活用するために、すべてのログファイルをPlatform Serverのログファイル(`PS::LogFolder`)と同じフォルダーに送信することをお勧めします。 初期設定は [!DNL logs/Supervisor.log].

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 必要な作成、読み取り、書き込み権限がサーバスーパーバイザに付与されるように、アクセス権限が設定されていることを確認します。

## SV::tracelevel — サーバスーパーバイザトレースログレベル {#section-36f8634741da4c618d67aa628b5fe474}

ログレベルは、1、2、3、4のいずれかです。 初期設定は 2 です

## IS::Log - Image Serverデバッグログファイルのパス {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Serverトレースログファイルのフォルダーとベースファイル名。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスで指定できます。 ImageServerは、ファイル名の前（存在する場合はファイルサフィックスの前）にハイフンと現在の日付(*[!DNL -yyyy-mm-dd]*)を追加します。 Platform Serverが実装したログファイル管理を活用するには、Image ServerのログファイルをPlatform Serverのログファイル(`PS::LogFolder`)と同じフォルダーに送信することをお勧めします（`PS::LogDays`を参照）。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 画像サービングに必要な作成、読み取り、書き込み権限が割り当てられるように、アクセス権限が設定されていることを確認します。

## IS:TraceClient - Image Serverデバッグログレベル {#section-3851f1f68e404430985c629ac80534db}

ログレベルは、1、2、3、4のいずれかです（デフォルトは2）。

レベル1では、起動、シャットダウン、およびPlatform Serverの接続に関するイベントが記録されます。

レベル2では、ソースイメージへの接続と切断もログに記録されます。

レベル3では、ピクセルデータに対する要求のログと、その配信のログがPlatform Serverに追加されます。

レベル4では、Platform Serverから受信したすべてのメッセージが記録されます。

ログファイルが非常に大きくなる可能性があるので、レベル3と4はデバッグ目的でのみ使用する必要があります。

## IS::TraceStatsInterval - Image Server統計ログの間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Serverは、この設定で指定された間隔で、メモリ統計をトレースログファイルに書き込みます。 有効な範囲は5 ～ 86,400秒です。
