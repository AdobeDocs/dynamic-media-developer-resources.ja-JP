---
description: トレースログをデバッグするには、次のサーバー設定を使用します。
seo-description: トレースログをデバッグするには、次のサーバー設定を使用します。
seo-title: Debug_traceログ
solution: Experience Manager
title: Debug_traceログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Debug_traceログ{#debug-trace-logging}

トレースログをデバッグするには、次のサーバー設定を使用します。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>と同じフォルダーに書き込まれるすべてのログファイルを設定することをお勧めしま `TC::directory`す。 これにより、すべての画像サービングのログファイルがで設定されたログファイルの自動ローテーションに含まれるようになり、ディスク領域不足によるサーバの不安定性を防ぐことがで `TC::maxDays`きます。

## SV::log — サーバスーパーバイザトレースログファイルのパス {#section-3697bc480ff646e79cacc2812c55ef26}

サーバスーパーバイザログファイルのフォルダとベースファイル名。 パスは、絶対パスまたは相対パスで指定できま *[!DNL install_folder]*&#x200B;す。 サーバスーパーバイザは、ファイル名にハイフンと現在の日付( *[!DNL -yyyy-mm-dd]*)を付加します（ファイル名の前にある場合は、その日付）。 Platform Server ( `PS::LogFolder`)が実装するログファイル管理を活用するために、すべてのログファイルをPlatform Serverのログファイル( `PS::LogDays`)と同じフォルダーに送信することをお勧めします。 初期設定は [!DNL logs/Supervisor.log].

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 サーバスーパーバイザが必要な作成、読み取り、書き込みの権限を持つように、アクセス権限が設定されていることを確認します。

## SV::tracelevel — サーバスーパーバイザトレースログレベル {#section-36f8634741da4c618d67aa628b5fe474}

ログレベルは1、2、3または4です。 初期設定は 2 です

## IS::Log - Image Serverデバッグログファイルのパス {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Serverトレースログファイルのフォルダーとベースファイル名。 パスは、絶対パスまたは相対パスで指定できま *[!DNL install_folder]*&#x200B;す。 ImageServerは、ファイル名にハイフンと現在の日付( *[!DNL -yyyy-mm-dd]*)を付加します（ファイル名の前にある場合は、その日付の前）。 Platform Serverによって実装されたログファイル管理を活用するため、Image ServerのログファイルをPlatform Serverのログファイル( `PS::LogFolder`)と同じフォルダに送信することをお勧めします(を参照し `PS::LogDays`てください)。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 画像サービングに必要な作成、読み取りおよび書き込み権限が与えられるように、アクセス権限が設定されていることを確認します。

## IS:TraceClient - Image Serverのデバッグログレベル {#section-3851f1f68e404430985c629ac80534db}

ログレベルは1、2、3または4（デフォルトは2）です。

レベル1は、起動、シャットダウン、およびプラットフォームサーバー接続に関するイベントを記録します。

レベル2は、ソースイメージへの接続と切断もログに記録します。

レベル3では、ピクセルデータの要求のログと、その要求の配信がプラットフォームサーバーに追加されます。

レベル4では、プラットフォームサーバーから受信したすべてのメッセージが記録されます。

ログファイルが非常に大きくなる可能性があるので、レベル3と4はデバッグ目的でのみ使用します。

## IS::TraceStatsInterval - Image Server統計ログの間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Serverは、この設定で指定された間隔で、メモリ統計をトレースログファイルに書き込みます。 有効な範囲は5 ～ 86,400秒です。
