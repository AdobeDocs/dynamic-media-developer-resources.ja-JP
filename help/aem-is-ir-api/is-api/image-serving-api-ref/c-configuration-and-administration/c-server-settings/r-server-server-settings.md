---
description: これらのサーバー設定を使用して、サーバーを構成します。
solution: Experience Manager
title: サーバ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# サーバ{#server}

これらのサーバー設定を使用して、サーバーを構成します。

## SV::ImageServerMode - Image Server モード {#section-991b287f2dde4f77a24fc69d5b32cabd}

Linux では、32 ビット版と 64 ビット版の両方の Image Server を使用できます。 64 ビットの Linux サーバーにインストールする場合は ImageServer64 を指定し、32 ビットのサーバーにインストールする場合は ImageServer32 （デフォルト）を指定します。

>[!NOTE]
>
>64 ビットバージョンの Image Server は、FlashPix ソースファイルをサポートしていません。

>[!NOTE]
>
>64 ビットモードは Windows ではサポートされていません。 `ImageServer32` のみを指定できます。 それ以外の場合、画像サービングは開始されません。

## SV::PsHeapSize - ヒープ サイズを [!DNL Platform Server] す {#section-fd83715948764aeda58d6b3a9f9f8be9}

[!DNL Platform Server] の Java ヒープサイズ。 デフォルトは「`512m`」（512 メガバイト）です。

## IS::TcpPort、PS::isConnection.port - Image Server のリスニングポート {#section-5421bfd2ca2a4a979faf812b6fdb2887}

[!DNL Platform Server] と Image Server 間の通信に使用するポートを指定します。 ホストシステムで使用されていないポート番号を指定してください。

>[!NOTE]
>
>画像サービングが正しく機能するには、`IS::TcpPort` と `PS::isConnection.port` に同じ値を設定する必要があります。

## IS::PhysicalMemory - Image Server のメモリ制限 {#section-85e37aa2ac6e456eb698da716dd3247d}

インメモリ画像データのおおよその上限（物理メモリに対する割合で表されます）。 有効な範囲は 10% ～ 90% です。 Image Server は、可能な場合、画像メモリの使用を指定された量に制限しようとします。 処理アクティビティが高い間は、一時的に制限を超える可能性があります。

## IS::WorkerThreads - Image Server ワーカーのThreadsの数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Image Server が画像データの処理に使用するスレッドの最大数。 デフォルトは 0 で、Image Server はスレッド数を自動的に最適化できます。

一部のオペレーティング システムには、コンテキスト切り替えのオーバーヘッドが大きいスレッド モデルがあります。 このような状況では、特定のスレッド数が選択されると（例えば、CPU ごとに 1 つのスレッド）、サーバーの全体的なパフォーマンスが向上する可能性があります。 最適な設定を見つけるには、いくつかの実験が必要になる場合があります。 詳しくは、画像サービングリリースノートおよびオペレーティングシステムのドキュメントを参照してください。

## IS::NumberOfTextServers - テキストサーバーインスタンスの数 {#section-971e20a90c1a473598fba738ed95671a}

同時にアクティブになるテキストレンダラーの最大数です。 0 （デフォルト）は、使用可能な CPU コアの数の 1.5 倍に相当します。

## IS::TextServerTcpPortRange - テキストサーバの通信ポート {#section-a13465de88ed4df09931e5ba840c1942}

テキスト サーバー通信に使用されるポートです。 最初と最後のポート番号を「–」で区切って指定します。
