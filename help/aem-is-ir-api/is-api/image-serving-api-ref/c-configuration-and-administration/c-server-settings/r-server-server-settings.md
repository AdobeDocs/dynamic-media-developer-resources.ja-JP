---
description: サーバーを設定するには、次のサーバー設定を使用します。
seo-description: サーバーを設定するには、次のサーバー設定を使用します。
seo-title: サーバ
solution: Experience Manager
title: サーバ
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# サーバ{#server}

サーバーを設定するには、次のサーバー設定を使用します。

## SV::ImageServerMode - Image Serverモード {#section-991b287f2dde4f77a24fc69d5b32cabd}

32ビット版と64ビット版の両方のImage ServerがLinuxで使用できます。 64ビットLinuxサーバにインストールする場合はImageServer64を、32ビットサーバにインストールする場合はImageServer32（デフォルト）を指定します。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>64ビット版のImage Serverは、FlashPixソースファイルをサポートしていません。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>64ビットモードはWindowsではサポートされていません。 指定で `ImageServer32` きるのはのみです。 そうしないと、画像サービングは開始されません。

## SV::PsHeapSize — プラットフォームサーバのヒープサイズ {#section-fd83715948764aeda58d6b3a9f9f8be9}

プラットフォームサーバーのJavaヒープサイズ。 デフォルトは「 `512m`」（512Mバイト）です。

## IS::TcpPort、PS::isConnection.port - Image Serverリスニングポート {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Platform ServerとImage Server間の通信に使用するポートを指定します。 ホストシステムでは使用されないポート番号を必ず指定してください。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>画像サービングが正しく機能するには、とに対して同じ値を設定する必要があ `IS::TcpPort` りま `PS::isConnection.port`す。

## IS::PhysicalMemory - Image Serverのメモリ制限 {#section-85e37aa2ac6e456eb698da716dd3247d}

メモリ内画像データの概算の限界値。物理メモリの割合で表されます。 有効な範囲は10% ～ 90%です。 Image Serverは、可能であれば、画像メモリの使用を指定した量に制限しようとします。 処理が多い場合は、この制限を一時的に超える可能性があります。

## IS::WorkerThreads - Image Serverのワーカスレッドの数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Image Serverが画像データの処理に使用するスレッドの最大数です。 初期設定は0で、Image Serverは自動的にスレッド数を最適化できます。

一部のオペレーティングシステムには、高いコンテキスト切り替えのオーバーヘッドを持つスレッドモデルが搭載されています。 このような状況では、特定のスレッド数（CPUあたり1つのスレッドなど）を選択すると、サーバの全体的なパフォーマンスが向上する可能性があります。 最適な設定を見つけるには、いくつかの実験が必要な場合があります。 詳しくは、画像サービングのリリースノートおよびオペレーティングシステムのドキュメントを参照してください。

## IS::NumberOfTextServers — テキストサーバーインスタンスの数 {#section-971e20a90c1a473598fba738ed95671a}

同時にアクティブにするテキストレンダラーの最大数です。 0（デフォルト）は、使用可能なCPUコアの数の1.5倍に相当します。

## IS::TextServerTcpPortRange — テキストサーバ通信ポート {#section-a13465de88ed4df09931e5ba840c1942}

テキストサーバー通信に使用するポート。 最初と最後のポート番号を「 — 」で区切って指定します。
