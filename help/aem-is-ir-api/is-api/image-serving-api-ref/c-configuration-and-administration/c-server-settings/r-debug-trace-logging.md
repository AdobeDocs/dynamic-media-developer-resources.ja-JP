---
title: Debug_trace ロギング
description: これらのサーバー設定を使用して、トレースログをデバッグします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
TQID: 'https://experienceleague.adobe.com/vkvp3WTt-nSSAQPaHUgXvMCuEkD-vEno-ot3Nxn9ReE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 0%

---

# Debug_trace ロギング{#debug-trace-logging}

これらのサーバー設定を使用して、トレースログをデバッグします。

>[!NOTE]
>
>Adobeでは、すべてのログファイルを`TC::directory`と同じフォルダーに書き込むように設定することをお勧めします。 これにより、すべてのImage Serving ログファイルが、`TC::maxDays`で設定された自動ログファイルのローテーションに参加することが保証され、ディスク領域不足によるサーバーの潜在的な不安定性を防ぐことができます。

## SV::log - Server Supervisor Trace Log File Path {#section-3697bc480ff646e79cacc2812c55ef26}

Server Supervisor ログ ファイルのフォルダーとベース ファイル名。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;からの相対パスにすることができます。 サーバースーパーバイザーは、ハイフンと現在の日付（*[!DNL -yyyy-mm-dd]*）をファイル名に追加します（ファイルのサフィックスがある場合は、その前）。 Adobeでは、すべてのログファイルを[!DNL Platform Server] ログファイル （`PS::LogFolder`）と同じフォルダーに送信して、[!DNL Platform Server] （`PS::LogDays`）によって実装されたログファイル管理を使用することをお勧めします。 デフォルトは[!DNL logs/Supervisor.log]です。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 サーバースーパーバイザーが必要な作成、読み取り、書き込み権限を持つように、アクセス権限が設定されていることを確認します。

## SV::tracelevel - Server Supervisor Trace Log Level {#section-36f8634741da4c618d67aa628b5fe474}

ログレベルは1、2、3、または4です。 デフォルトは2です。

## IS::Log - Image Server Debug Log File Path {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Server トレースログファイルのフォルダーとベースファイル名。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;からの相対パスにすることができます。 ImageServerは、ハイフンと現在の日付（*[!DNL -yyyy-mm-dd]*）をファイル名に追加します（ファイルのサフィックスがある場合は、その前）。 Adobeでは、[!DNL Platform Server]によって実装されたログファイル管理を使用するために、[!DNL Platform Server] ログファイル （`PS::LogFolder`）と同じフォルダーにImage Server ログファイルを送信することをお勧めします（`PS::LogDays`を参照）。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 Image Servingに必要な作成、読み取り、書き込み権限が付与されるように、アクセス権限が設定されていることを確認します。

## IS:TraceClient - イメージ サーバーのデバッグ ログ レベル {#section-3851f1f68e404430985c629ac80534db}

ログレベルは1、2、3、または4です（デフォルトは2）

レベル 1では、起動、シャットダウン、および[!DNL Platform Server]接続に関連するイベントがログに記録されます。

レベル 2では、ソース画像との接続と切断もログに記録されます。

レベル 3では、ピクセルデータのリクエストのログを追加し、それを[!DNL Platform Server]に配信します。

レベル 4は、[!DNL Platform Server]から受信したすべてのメッセージを記録します。

ログファイルが大きくなる可能性があるため、レベル 3と4はデバッグ目的でのみ使用してください。

## IS::TraceStatsInterval - Image Server Statistics Log Interval {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Serverは、この設定で指定された間隔でメモリ統計をトレース ログ ファイルに書き込みます。 有効な範囲は5 ～ 86,400秒です。
