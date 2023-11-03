---
description: これらのサーバー設定を使用して、サーバーを設定します。
solution: Experience Manager
title: サーバ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# サーバ{#server}

これらのサーバー設定を使用して、サーバーを設定します。

## SV::ImageServerMode - Image Server Mode {#section-991b287f2dde4f77a24fc69d5b32cabd}

Image Server の 32 ビット版と 64 ビット版の両方が Linux で利用できます。 64 ビット Linux サーバーにインストールする場合は ImageServer64 を指定し、32 ビットサーバーにインストールする場合は ImageServer32（デフォルト）を指定します。

>[!NOTE]
>
>64 ビット版の Image Server は、FlashPix ソースファイルをサポートしていません。

>[!NOTE]
>
>Windows では、64 ビットモードはサポートされていません。 のみ `ImageServer32` を指定できます。 そうしないと、画像サービングが開始されません。

## SV::PsHeapSize - [!DNL Platform Server] ヒープサイズ {#section-fd83715948764aeda58d6b3a9f9f8be9}

の Java ヒープサイズ [!DNL Platform Server]. デフォルト値は&quot; `512m`&quot; （512M バイト）

## IS::TcpPort, PS::isConnection.port - Image Server リスニングポート {#section-5421bfd2ca2a4a979faf812b6fdb2887}

間の通信に使用するポートを指定します [!DNL Platform Server] と Image Server ホストシステムで他の方法で使用されないポート番号を必ず指定してください。

>[!NOTE]
>
>画像サービングが正しく機能するには、 `IS::TcpPort` および `PS::isConnection.port`.

## IS::PhysicalMemory - Image Server のメモリ制限 {#section-85e37aa2ac6e456eb698da716dd3247d}

物理メモリの割合で表される、インメモリイメージデータの近似制限。 有効な範囲は 10%～ 90%です。 Image Server は、イメージメモリの使用を、指定可能な場合は指定した量に制限しようとします。 この制限は、処理アクティビティが多い間、一時的に超える場合があります。

## IS::WorkerThreads - Image Server ワーカーThreadsの数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Image Server が画像データの処理に使用するスレッドの最大数です。 初期設定は 0 で、Image Server は自動的にスレッド数を最適化できます。

一部のオペレーティングシステムでは、高いコンテキストスイッチングオーバーヘッドを持つスレッディングモデルが搭載されています。 このような状況では、特定のスレッド数を選択すると（CPU 1 つにつき 1 つのスレッドが選択されるなど）、サーバー全体のパフォーマンスが向上する場合があります。 最適な設定を見つけるには、いくつかの実験が必要になる場合があります。 詳しくは、画像サービングのリリースノートおよびオペレーティングシステムのドキュメントを参照してください。

## IS::NumberOfTextServers — テキストサーバーインスタンスの数 {#section-971e20a90c1a473598fba738ed95671a}

同時にアクティブにするテキストレンダラーの最大数。 0 （デフォルト）は、使用可能な CPU コアの数の 1.5 倍に相当します。

## IS::TextServerTcpPortRange — テキストサーバ通信ポート {#section-a13465de88ed4df09931e5ba840c1942}

テキストサーバー通信に使用するポート。 最初と最後のポート番号を「 — 」で区切って指定します。
