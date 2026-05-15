---
description: これらのサーバー設定を使用して、サーバーを設定します。
solution: Experience Manager
title: サーバ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
TQID: 'https://experienceleague.adobe.com/403CInOL4425Gv35Njb69WSo-QRyvTuDUZEBtNRsvj0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 357
ht-degree: 0%

---

# サーバ{#server}

これらのサーバー設定を使用して、サーバーを設定します。

## SV::ImageServerMode - Image Server Mode {#section-991b287f2dde4f77a24fc69d5b32cabd}

Linuxでは、32 ビット版と64 ビット版の両方のImage Serverを利用できます。 64 ビット Linux サーバーにインストールする場合はImageServer64を、32 ビットサーバーにインストールする場合はImageServer32 （デフォルト）を指定します。

>[!NOTE]
>
>64 ビット版のImage Serverは、FlashPix ソースファイルをサポートしていません。

>[!NOTE]
>
>64 ビットモードはWindowsではサポートされていません。 `ImageServer32`のみを指定できます。 それ以外の場合、画像サービングは開始されません。

## SV::PsHeapSize - [!DNL Platform Server] ヒープサイズ {#section-fd83715948764aeda58d6b3a9f9f8be9}

[!DNL Platform Server]のJava ヒープサイズ。 デフォルトは&quot; `512m`&quot; （512 M バイト）です。

## IS::TcpPort, PS::isConnection.port - Image Server Listening Port {#section-5421bfd2ca2a4a979faf812b6fdb2887}

[!DNL Platform Server]とImage Server間の通信に使用するポートを指定します。 ホストシステムで使用されていないポート番号を指定してください。

>[!NOTE]
>
>画像サービングを正しく機能させるには、`IS::TcpPort`と`PS::isConnection.port`に同じ値を設定する必要があります。

## IS::PhysicalMemory - イメージ サーバーのメモリ制限 {#section-85e37aa2ac6e456eb698da716dd3247d}

メモリ内の画像データの概算リミット。物理メモリの割合で表されます。 有効な範囲は10 ～ 90%です。 Image Serverは、可能であれば、画像メモリの使用を指定された量に制限しようとします。 処理量が多い場合、制限を一時的に超える可能性があります。

## IS::WorkerThreads - Image Server Worker Threadsの数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Image Serverが画像データの処理に使用するスレッドの最大数。 デフォルトは0で、Image Serverはスレッド数を自動的に最適化できます。

一部のオペレーティングシステムでは、コンテクスト切り替えのオーバーヘッドが高いスレッディングモデルを備えています。 このような場合、特定のスレッド数（例えば、CPUごとに1つのスレッド）を選択すると、サーバー全体のパフォーマンスが向上する可能性があります。 最適な設定を見つけるために、ある程度の実験が必要になる場合があります。 詳しくは、Image Serving リリースノートおよびオペレーティングシステムのドキュメントを参照してください。

## IS::NumberOfTextServers - Text Server インスタンスの数 {#section-971e20a90c1a473598fba738ed95671a}

同時にアクティブになるテキストレンダラーの最大数。 0 （デフォルト）は、使用可能なCPU コアの数の1.5倍に相当します。

## IS::TextServerTcpPortRange - テキスト サーバー通信ポート {#section-a13465de88ed4df09931e5ba840c1942}

テキストサーバー通信に使用するポート。 最初と最後のポート番号を「 – 」で区切って指定します。
