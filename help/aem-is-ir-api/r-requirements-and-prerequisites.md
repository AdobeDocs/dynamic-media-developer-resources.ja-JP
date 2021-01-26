---
description: Dynamic Media画像サービングを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。
seo-description: Dynamic Media画像サービングを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。
seo-title: 必要システム構成と前提条件
solution: Experience Manager
title: 必要システム構成と前提条件
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---


# 必要システム構成と前提条件{#system-requirements-and-prerequisites}

Dynamic Media画像サービングを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。

## サーバハードウェア{#section-f3c14a7bc1b745118602659628df779f}

お使いのサーバは、次のハードウェア要件を満たしている必要があります。

>[!NOTE]
>
>AMD64およびインテル® EM64Tを搭載したプロセッサーを搭載したシステムは、通常、NUMA(Non-Uniform Memory Architecture)プラットフォームとして構成されます。 これは、カーネルが起動時に、単一のメモリノードを構築するのではなく、複数のメモリノードを構築することを意味します。 複数のノード構成体は、他のノードが消耗する前に、1つ以上のノードでメモリが消耗する可能性があります。 メモリ不足が発生した場合、カーネルは、メモリが空いていてもプロセス（Image ServerやPlatform Serverなど）をキルすることを決定できます。 したがって、Adobe Systemsでは、このようなシステムを実行している場合はNUMAをオフにすることをお勧めします。 `numa=off`開始オプションを使用して、カーネルがこれらのプロセスを停止しないようにします。

**Windows**

* Intel Xeon®またはAMD® Opteron CPU、少なくとも4コア。
* 16 GB以上のRAM。
* スワップ空間は、物理メモリ(RAM)の少なくとも2倍に等しい。
* 2 GBのハードディスク空き容量（インストールと基本操作に必要）。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加のディスク空き容量が必要です。
* Fast Ethernet Network Interface Card。

**Linux**

* Intel Xeon®またはAMD® Opteron CPU、少なくとも4コア。
* 16 GB以上のRAM。
* スワップは無効（推奨）
* 2 GBのハードディスク空き容量（インストールと基本操作に必要）。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加のディスク空き容量が必要です。
* Fast Ethernet Network Interface Card。

**注意(Linux):** 画像サービングは、SELinuxをオンにしても機能しません。このオプションはデフォルトで有効になっています。 SELinuxを無効にするには、[!DNL /etc/selinux/config]ファイルを編集し、SELinux値を次の値から変更します。

`SELINUX=enforcing`

へ

`SELINUX=disabled`

**注意(Linux)：サーバーのホスト名がIPアドレスに解決できることを** 確認してください。これが不可能な場合は、次の例のように、[!DNL /etc/hosts]に完全修飾ホスト名とIPアドレスを追加します。

`<ip address> <fully qualified hostname>`

## サーバーソフトウェア{#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media画像サービングには、次のサーバソフトウェアが必要です。

**Windows**

* Microsoft® Windows 2008 Server。
* 64ビットのオペレーティングシステム。

**Linux**

* Red Hat® Enterprise 5またはCentOS 5.5以降、最新の修正パッチが適用されています。
* 64ビットのオペレーティングシステム。

**注意：Windows** で画像サービングを使用するには、Microsoft Visual Studio 2010再配布可能版をインストールする必要があります。再頒布可能パッケージは次の場所で入手できます。

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

