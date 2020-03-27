---
description: Scene7画像サービングを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。
seo-description: Scene7画像サービングを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。
seo-title: 必要システム構成と前提条件
solution: Experience Manager
title: 必要システム構成と前提条件
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 必要システム構成と前提条件{#system-requirements-and-prerequisites}

Scene7画像サービングを使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。

## サーバハードウェア {#section-f3c14a7bc1b745118602659628df779f}

お使いのサーバは、次のハードウェア要件を満たしている必要があります。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>AMD64およびIntel® EM64Tを搭載したプロセッサーを搭載したシステムは、通常、NUMA(Non-Uniform Memory Architecture)プラットフォームとして構成されます。 つまり、カーネルは単一のメモリノードを構築するのではなく、起動時に複数のメモリノードを構築します。 複数ノード構成体は、他のノードが消耗する前に、1つ以上のノードのメモリを消耗させる可能性がある。 メモリが枯渇した場合は、使用可能なメモリがあっても、カーネルはプロセス（Image ServerやPlatform Serverなど）を強制終了することができます。 したがって、アドビシステムズ社では、このようなシステムを実行している場合はNUMAをオフにすることをお勧めします。 カーネルがこれ `numa=off` らのプロセスを停止しないようにするには、startオプションを使用します。

**Windows**

* Intel Xeon®またはAMD® Opteron CPU、4コア以上。
* 16 GB以上のRAM。
* スワップ領域は、物理メモリ(RAM)の少なくとも2倍に等しい。
* 2 GBの空き容量のあるハードディスクは、インストールと基本操作に使用できます。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加の空き容量が必要です。
* ファストイーサネットネットワークインターフェイスカード。

**Linux**

* Intel Xeon®またはAMD® Opteron CPU、4コア以上。
* 16 GB以上のRAM。
* スワップが無効（推奨）。
* 2 GBの空き容量のあるハードディスクは、インストールと基本操作に使用できます。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加の空き容量が必要です。
* ファストイーサネットネットワークインターフェイスカード。

**注意(Linux):** SELinuxがオンの場合、画像サービングは機能しません。 このオプションはデフォルトで有効です。 SELinuxを無効にするには、ファイルを編 [!DNL /etc/selinux/config] 集し、SELinux値を次のように変更します。

`SELINUX=enforcing`

へ

`SELINUX=disabled`

**注意(Linux):** サーバーのホスト名がIPアドレスに解決できることを確認します。 これが不可能な場合は、次の例のように、に完全修飾ホスト名とIPア [!DNL /etc/hosts] ドレスを追加します。

`<ip address> <fully qualified hostname>`

## サーバソフトウェア {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Scene7画像サービングには、次のサーバソフトウェアが必要です。

**Windows**

* Microsoft® Windows 2008 Server。
* 64ビットオペレーティングシステム。

**Linux**

* Red Hat® Enterprise 5またはCentOS 5.5以降、最新の修正パッチが適用されています。
* 64ビットオペレーティングシステム。

**注意：** Windowsで画像サービングを使用するには、Microsoft Visual Studio 2010再配布可能ファイルをインストールする必要があります。 再頒布可能パッケージは次の場所で入手できます。

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

