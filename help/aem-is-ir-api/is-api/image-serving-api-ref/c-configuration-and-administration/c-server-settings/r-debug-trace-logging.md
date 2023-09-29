---
title: Debug_trace ログ
description: トレースログをデバッグするには、これらのサーバー設定を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Debug_trace ログ{#debug-trace-logging}

トレースログをデバッグするには、これらのサーバー設定を使用します。

>[!NOTE]
>
>Adobeでは、 `TC::directory`. これにより、すべての画像サービングログファイルが、 `TC::maxDays`：ディスク容量不足によるサーバーの不安定性を防ぎます。

## SV::log — サーバスーパーバイザトレースログファイルのパス {#section-3697bc480ff646e79cacc2812c55ef26}

サーバスーパーバイザログファイルのフォルダとベースファイル名。 パスは、絶対パスまたは相対パスにすることができます。 *[!DNL install_folder]*. サーバスーパーバイザは、ハイフンと現在の日付 ( *[!DNL -yyyy-mm-dd]*) をファイル名（ファイルサフィックスの前、存在する場合はその後）に追加します。 Adobeでは、 [!DNL Platform Server] ログファイル ( `PS::LogFolder`) を使用して、 [!DNL Platform Server] (`PS::LogDays`) をクリックします。 デフォルトはです。 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 サーバスーパーバイザが必要な作成、読み取り、書き込みの権限を持つように、アクセス権限が設定されていることを確認します。

## SV::tracelevel — サーバスーパーバイザトレースログレベル {#section-36f8634741da4c618d67aa628b5fe474}

ログレベルは、1、2、3、4 のいずれかです。 初期設定値は 2 です。

## IS::Log - Image Server デバッグログファイルのパス {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Server トレースログファイルのフォルダとベースファイル名。 パスは、絶対パスまたは相対パスにすることができます。 *[!DNL install_folder]*. ImageServer は、ハイフンと現在の日付 ( *[!DNL -yyyy-mm-dd]*) をファイル名（ファイルサフィックスの前、存在する場合はその後）に追加します。 Adobeでは、Image Server のログファイルを [!DNL Platform Server] ログファイル ( `PS::LogFolder`) を使用して、 [!DNL Platform Server] ( `PS::LogDays`) をクリックします。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 画像サービングに必要な作成、読み取りおよび書き込み権限が付与されるように、アクセス権限が設定されていることを確認します。

## IS:TraceClient - Image Server デバッグログレベル {#section-3851f1f68e404430985c629ac80534db}

ログレベルは 1、2、3、4 のいずれかです（デフォルトは 2）。

レベル 1 では、開始、シャットダウン、および [!DNL Platform Server] 接続。

レベル 2 では、ソース画像との接続と切断もログに記録されます。

レベル 3 では、ピクセルデータの要求のログと、その配信のログが [!DNL Platform Server].

レベル 4 では、 [!DNL Platform Server].

ログファイルが大きくなる可能性があるので、レベル 3 と 4 はデバッグ目的でのみ使用する必要があります。

## IS::TraceStatsInterval - Image Server 統計ログの間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Server は、この設定で指定された間隔で、メモリ統計をトレースログファイルに書き込みます。 有効な範囲は 5 ～ 86,400 秒です。
