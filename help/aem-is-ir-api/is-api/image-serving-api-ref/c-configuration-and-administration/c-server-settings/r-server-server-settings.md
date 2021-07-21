---
description: これらのサーバー設定を使用して、サーバーを設定します。
solution: Experience Manager
title: サーバ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# サーバ{#server}

これらのサーバー設定を使用して、サーバーを設定します。

## SV::ImageServerMode - Image Serverモード {#section-991b287f2dde4f77a24fc69d5b32cabd}

Image Serverの32ビット版と64ビット版の両方がLinuxで使用できます。 64ビットLinuxサーバーにインストールする場合はImageServer64を指定し、32ビットサーバーにインストールする場合はImageServer32（デフォルト）を指定します。

>[!NOTE]
>
>64ビット版のImage Serverは、FlashPixソースファイルをサポートしていません。

>[!NOTE]
>
>64ビットモードは、Windowsではサポートされていません。 `ImageServer32`のみを指定できます。 そうしないと、画像サービングが開始されません。

## SV::PsHeapSize — プラットフォームサーバのヒープサイズ {#section-fd83715948764aeda58d6b3a9f9f8be9}

Platform ServerのJavaヒープサイズ。 デフォルトは「 `512m` 」（512Mバイト）です。

## IS::TcpPort, PS::isConnection.port - Image Serverリスニングポート {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Platform ServerとImage Server間の通信に使用するポートを指定します。 ホストシステム上で他の方法で使用されないポート番号を必ず指定してください。

>[!NOTE]
>
>画像サービングが正しく機能するには、`IS::TcpPort`と`PS::isConnection.port`に同じ値を設定する必要があります。

## IS::PhysicalMemory - Image Serverのメモリ制限 {#section-85e37aa2ac6e456eb698da716dd3247d}

メモリ内画像データの概算制限。物理メモリの割合で表されます。 有効な範囲は10%～ 90%です。 Image Serverは、可能な場合は、イメージメモリの使用を指定した量に制限しようとします。 この制限は、処理アクティビティが多い間に一時的に超える可能性があります。

## IS::WorkerThreads - Image Serverワーカースレッド数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Image Serverが画像データの処理に使用するスレッドの最大数。 初期設定は0で、Image Serverはスレッド数を自動的に最適化できます。

一部のオペレーティングシステムには、高いコンテキスト切り替えオーバーヘッドを持つスレッディングモデルがあります。 このような状況では、特定のスレッド数（CPUあたり1スレッド）を選択すると、サーバー全体のパフォーマンスが向上する場合があります。 最適な設定を見つけるには、いくつかの実験が必要になる場合があります。 詳しくは、画像サービングのリリースノートおよびオペレーティングシステムのドキュメントを参照してください。

## IS::NumberOfTextServers — テキストサーバーインスタンスの数 {#section-971e20a90c1a473598fba738ed95671a}

同時にアクティブにするテキストレンダラーの最大数。 0 （デフォルト）は、使用可能なCPUコアの1.5倍に相当します。

## IS::TextServerTcpPortRange — テキストサーバの通信ポート {#section-a13465de88ed4df09931e5ba840c1942}

テキストサーバー通信に使用するポート。 最初と最後のポート番号を「 — 」で区切って指定します。
