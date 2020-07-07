---
description: これらのサーバー設定を使用して、サーバーを設定します。
seo-description: これらのサーバー設定を使用して、サーバーを設定します。
seo-title: サーバ
solution: Experience Manager
title: サーバ
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# サーバ{#server}

これらのサーバー設定を使用して、サーバーを設定します。

## SV::ImageServerMode - Image Serverモード {#section-991b287f2dde4f77a24fc69d5b32cabd}

32ビット版と64ビット版の両方のImage ServerがLinuxで利用できます。 64ビットLinuxサーバーにインストールする場合はImageServer64を、32ビットサーバーにインストールする場合はImageServer32（初期設定）を指定します。

>[!NOTE]
>
>64ビット版のImage Serverは、FlashPixソースファイルをサポートしていません。

>[!NOTE]
>
>64ビットモードはWindowsではサポートされていません。 のみ指定 `ImageServer32` できます。 そうしないと、画像サービングは開始しません。

## SV::PsHeapSize -Platformサーバーのヒープサイズ {#section-fd83715948764aeda58d6b3a9f9f8be9}

PlatformサーバーのJavaヒープサイズです。 デフォルトは「 `512m`」（512Mバイト）です。

## IS::TcpPort、PS::isConnection.port - Image Serverリスニングポート {#section-5421bfd2ca2a4a979faf812b6fdb2887}

PlatformサーバとImage Server間の通信に使用するポートを指定します。 ホストシステムでは使用されないポート番号を指定してください。

>[!NOTE]
>
>画像サービングが正しく機能するためには、とに対して同じ値を設定する必要があり `IS::TcpPort` ま `PS::isConnection.port`す。

## IS::PhysicalMemory - Image Serverのメモリ制限 {#section-85e37aa2ac6e456eb698da716dd3247d}

メモリ内画像データの概算制限。物理メモリに対する割合で表されます。 有効な範囲は10% ～ 90%です。 Image Serverは、可能であれば、イメージメモリの使用を指定した量に制限しようとします。 大量の処理アクティビティ中は、この制限を一時的に超える場合があります。

## IS::WorkerThreads - Image Serverのワーカースレッド数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Image Serverが画像データを処理する際に使用するスレッドの最大数です。 初期設定は0で、Image Serverは自動的にスレッド数を最適化できます。

一部のオペレーティングシステムには、高いコンテキスト切り替えオーバーヘッドを持つスレッディングモデルがあります。 このような状況では、特定のスレッド数（例えば、CPUあたり1スレッド）を選択すると、サーバ全体のパフォーマンスが向上する可能性があります。 最適な設定を見つけるには、いくつかの実験が必要になる場合があります。 詳しくは、画像サービングのリリースノートおよびオペレーティングシステムのドキュメントを参照してください。

## IS::NumberOfTextServers — テキストサーバーインスタンスの数 {#section-971e20a90c1a473598fba738ed95671a}

同時にアクティブにするテキストレンダラーの最大数。 0（デフォルト）は、使用可能なCPUコアの数の1.5倍に相当します。

## IS::TextServerTcpPortRange — テキストサーバー通信ポート {#section-a13465de88ed4df09931e5ba840c1942}

テキストサーバーとの通信に使用するポート。 最初と最後のポート番号を「 — 」で区切って指定します。
