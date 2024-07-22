---
title: Debug_trace ログ
description: これらのサーバー設定を使用して、トレース ログをデバッグします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Debug_trace ログ{#debug-trace-logging}

これらのサーバー設定を使用して、トレース ログをデバッグします。

>[!NOTE]
>
>Adobeでは、すべてのログファイルを `TC::directory` と同じフォルダーに書き込むように設定することをお勧めします。 これにより、すべての画像サービングログファイルが、`TC::maxDays` で設定されたログファイルの自動ローテーションに関与するようになり、ディスク容量不足によるサーバーの不安定を防ぐことができます。

## SV::log - サーバースーパーバイザートレース ログ ファイルのパス {#section-3697bc480ff646e79cacc2812c55ef26}

サーバースーパーバイザーログファイルのフォルダーとベースファイル名。 パスは絶対パスでも、*[!DNL install_folder]* からの相対パスでも構いません。 サーバースーパーバイザーは、ファイル名にハイフンと現在の日付（*[!DNL -yyyy-mm-dd]*）を（存在する場合はファイルサフィックスの前に）追加します。 Adobeでは、[!DNL Platform Server] （`PS::LogDays`）で実装されているログファイル管理を使用するために、すべてのログファイルを [!DNL Platform Server] ログファイル（`PS::LogFolder`）と同じフォルダーに送信することをお勧めします。 デフォルトは [!DNL logs/Supervisor.log] です。

>[!NOTE]
>
>この設定を変更する前に、新規フォルダーを作成する必要があります。 サーバースーパーバイザーが必要な作成、読み取りおよび書き込み権限を持つように、アクセス権限が設定されていることを確認します。

## SV::tracelevel - サーバースーパーバイザートレース ログ レベル {#section-36f8634741da4c618d67aa628b5fe474}

ログレベルは 1、2、3、4 のいずれかです。 初期設定値は 2 です。

## IS::Log - Image Server デバッグ ログ ファイルのパス {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Server のトレースログファイルのフォルダーとベースファイル名。 パスは絶対パスでも、*[!DNL install_folder]* からの相対パスでも構いません。 ImageServer は、ファイル名（存在する場合はファイルサフィックスの前）にハイフンと現在の日付（*[!DNL -yyyy-mm-dd]*）を追加します。 Adobeでは、[!DNL Platform Server] が実装したログファイル管理を使用するために、Image Server ログファイルを [!DNL Platform Server] ログファイル（`PS::LogFolder`）と同じフォルダーに送信することをお勧めします（`PS::LogDays` を参照）。

>[!NOTE]
>
>この設定を変更する前に、新規フォルダーを作成する必要があります。 画像サービングが必要な作成、読み取りおよび書き込み権限を持つように、アクセス権限が設定されていることを確認します。

## IS:TraceClient - Image Server のデバッグログレベル {#section-3851f1f68e404430985c629ac80534db}

ログレベルは 1、2、3、4 のいずれかです（デフォルトは 2）

レベル 1 のログには、接続の開始、シャットダウン、[!DNL Platform Server] ストに関するイベントが記録されます。

レベル 2 では、ソース画像への接続とソース画像からの切断もログに記録されます。

レベル 3 では、ピクセルデータのリクエストのログと、そのデータの [!DNL Platform Server] への配信が追加されます。

レベル 4 は、[!DNL Platform Server] ーバーから受信したすべてのメッセージを記録します。

ログファイルが大きくなる可能性があるので、レベル 3 と 4 はデバッグ目的でのみ使用してください。

## IS::TraceStatsInterval - Image Server の統計情報ログの間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Server は、この設定で指定された間隔で、メモリ統計をトレースログファイルに書き込みます。 有効な範囲は 5～86,400 秒です。
