---
description: Dynamic Media Image Servingを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。
solution: Experience Manager
title: 必要システム構成と前提条件
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 必要システム構成と前提条件{#system-requirements-and-prerequisites}

Dynamic Media Image Servingを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。

## サーバハードウェア {#section-f3c14a7bc1b745118602659628df779f}

サーバは、次のハードウェア要件を満たす必要があります。

>[!NOTE]
>
>AMD64およびIntel® EM64Tを搭載したプロセッサを搭載したシステムは、通常、NUMA(Non-Uniform Memory Architecture)プラットフォームとして構成されます。 つまり、カーネルは、単一のメモリノードを構築するのではなく、ブート時に複数のメモリノードを構築します。 複数のノード構成体は、他のノードが使い果たされる前に、1つ以上のノードでメモリが枯渇する可能性があります。 メモリが枯渇した場合、カーネルは、使用可能なメモリがあるにもかかわらず、プロセス（例えば、Image ServerやPlatform Serverなど）を強制終了することを決定できます。 したがって、Adobe Systemsでは、このようなシステムを実行している場合はNUMAをオフにすることをお勧めします。 `numa=off` startオプションを使用して、カーネルがこれらのプロセスを停止しないようにします。

**Windows**

* Intel Xeon®またはAMD® Opteron CPUと4コア以上。
* 16 GB以上のRAM
* スワップ領域は、物理メモリ(RAM)の少なくとも2倍の容量に等しい。
* インストールと基本操作に2 GBのハードディスク空き容量が必要です。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加のディスク容量が必要です。
* Fast Ethernet Network Interface Card。

**Linux**

* Intel Xeon®またはAMD® Opteron CPUと4コア以上。
* 16 GB以上のRAM
* スワップが無効（推奨）
* インストールと基本操作に2 GBのハードディスク空き容量が必要です。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加のディスク容量が必要です。
* Fast Ethernet Network Interface Card。

**注意(Linux):** 画像サービングは、SELinuxがオンの場合は機能しません。このオプションは、デフォルトで有効になっています。 SELinuxを無効にするには、[!DNL /etc/selinux/config]ファイルを編集し、SELinux値を次の値から変更します。

`SELINUX=enforcing`

へ

`SELINUX=disabled`

**注意(Linux):** サーバーのホスト名がIPアドレスに解決できることを確認してください。これができない場合は、次の例に示すように、完全修飾ホスト名とIPアドレスを[!DNL /etc/hosts]に追加します。

`<ip address> <fully qualified hostname>`

## サーバ・ソフトウェア {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Mediaの画像サービングには、次のサーバーソフトウェアが必要です。

**Windows**

* Microsoft® Windows 2008 Server
* 64ビットオペレーティングシステム。

**Linux**

* Red Hat® Enterprise 5またはCentOS 5.5以降（最新の修正パッチを適用済み）。
* 64ビットオペレーティングシステム。

**注意：** Windowsで画像サービングを使用するには、Microsoft Visual Studio 2010の再頒布可能パッケージをインストールする必要があります。再頒布可能パッケージは次の場所で入手できます。

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)
