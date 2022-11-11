---
description: Dynamic Media Image Serving を使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。
solution: Experience Manager
title: 必要システム構成と前提条件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 必要システム構成と前提条件{#system-requirements-and-prerequisites}

Dynamic Media Image Serving を使用する前に、お使いのシステムが必要システム構成を満たしていることを確認してください。

## サーバハードウェア {#section-f3c14a7bc1b745118602659628df779f}

お使いのサーバは、次のハードウェア要件を満たしている必要があります。

>[!NOTE]
>
>AMD64 および Intel® EM64Tを搭載したプロセッサを搭載したシステムは、通常、NUMA(Non-Uniform Memory Architecture) プラットフォームとして構成されます。 つまり、カーネルは、単一のメモリノードを構築するのではなく、ブート時に複数のメモリノードを構築します。 複数のノード構成体を使用すると、他のノードが消費される前に、1 つ以上のノードでメモリが枯渇する可能性があります。 メモリが枯渇した場合、カーネルはプロセス ( 例えば、Image Server や [!DNL Platform Server]) を返します。 したがって、Adobe Systemsでは、このようなシステムを実行している場合は、NUMA をオフにすることをお勧めします。 以下を使用： `numa=off` カーネルがこれらのプロセスを停止しないようにするための start オプション。

**Windows**

* Intel Xeon®または AMD® Opteron CPU と 4 コア以上。
* 16 GB 以上の RAM
* スワップ領域は、物理メモリ (RAM) の少なくとも 2 倍の容量に等しい。
* インストールと基本操作に 2 GB の空きハードディスク容量が必要です。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加のディスク容量が必要です。
* Fast Ethernet Network Interface Card（ファーストイーサネットネットワークインターフェイスカード）

**Linux**

* Intel Xeon®または AMD® Opteron CPU と 4 コア以上。
* 16 GB 以上の RAM
* スワップ無効（推奨）。
* インストールと基本操作に 2 GB の空きハードディスク容量が必要です。ソースイメージ、ログ、データキャッシュ、マニフェストファイルには、追加のディスク容量が必要です。
* Fast Ethernet Network Interface Card（ファーストイーサネットネットワークインターフェイスカード）

**注意 (Linux):** SELinux がオンの場合、画像サービングは機能しません。 このオプションは、デフォルトで有効になっています。 SELinux を無効にするには、 [!DNL /etc/selinux/config] ファイルを開き、SELinux 値を次の値から変更します。

`SELINUX=enforcing`

へ

`SELINUX=disabled`

**注意 (Linux):** サーバーのホスト名が IP アドレスに解決できることを確認します。 これができない場合は、完全修飾ホスト名と IP アドレスをに追加します。 [!DNL /etc/hosts] を次の例のように使用します。

`<ip address> <fully qualified hostname>`

## サーバソフトウェア {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Mediaの画像サービングには、次のサーバーソフトウェアが必要です。

**Windows**

* Microsoft® Windows 2008 Server
* 64 ビットオペレーティングシステム。

**Linux**

* Red Hat® Enterprise 5 または CentOS 5.5 以降（最新の修正パッチを適用）。
* 64 ビットオペレーティングシステム。

**注意：** Windows で画像サービングを使用するには、Microsoft Visual Studio 2010 の再頒布可能パッケージをインストールする必要があります。
