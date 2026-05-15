---
title: 必要システム構成と前提条件
description: Dynamic Media画像サービングを使用する前に、システムが必要システム構成を満たしていることを確認してください。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
TQID: 'https://experienceleague.adobe.com/SKAe9OsVsSkTRR5E3s5lBcPct4CgG1h1uIh7ayIpINA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 390
ht-degree: 0%

---

# 必要システム構成と前提条件{#system-requirements-and-prerequisites}

Dynamic Media画像サービングを使用する前に、システムが必要システム構成を満たしていることを確認してください。

## サーバーハードウェア {#section-f3c14a7bc1b745118602659628df779f}

サーバーは、次のハードウェア要件を満たしている必要があります。

>[!NOTE]
>
>AMD64とインテル® EM64Tを搭載したプロセッサー搭載システムは、通常、NUMA （Non-Uniform Memory Architecture）プラットフォームとして構成されます。 これは、カーネルが単一のメモリノードを構築するのではなく、起動時に複数のメモリノードを構築することを意味します。 複数ノード構成体は、他のノードが消耗する前に、1つ以上のノードのメモリ消耗を引き起こす可能性がある。 メモリ不足が発生すると、使用可能なメモリがあるにもかかわらず、カーネルはプロセス （Image Serverや[!DNL Platform Server]など）を強制終了できます。 したがって、Adobeでは、そのようなシステムを実行している場合はNUMAをオフにすることをお勧めします。 カーネルがこれらのプロセスを停止しないようにするには、`numa=off`開始オプションを使用します。

**Windows**

* Intel Xeon®またはAMD® Opteron CPU（少なくとも4 コア）。
* 1 GB以上のRAM。
* スワップ領域は、物理メモリ（RAM）の少なくとも2倍に相当します。
* インストールと基本操作のために2 GBのハードディスク空き容量が必要です。ソースイメージ、ログ、データキャッシュ、およびマニフェストファイルには、追加のディスク空き容量が必要です。
* 高速イーサネットネットワークインターフェイスカード。

**Linux®**

* Intel Xeon®またはAMD® Opteron CPU（少なくとも4 コア）。
* 16 GB以上のRAM。
* スワップは無効（推奨）です。
* インストールと基本操作のために2 GBのハードディスク空き容量が必要です。ソースイメージ、ログ、データキャッシュ、およびマニフェストファイルには、追加のディスク空き容量が必要です。
* 高速イーサネットネットワークインターフェイスカード。

**メモ （Linux®）:**&#x200B;画像サービングは、SELinuxをオンにすると機能しません。 このオプションはデフォルトで有効になっています。 SELinuxを無効にするには、[!DNL /etc/selinux/config] ファイルを編集し、SELinux値を次のように変更します。

`SELINUX=enforcing`

へ

`SELINUX=disabled`

**メモ （Linux®）:** サーバーのホスト名がIP アドレスに解決可能であることを確認します。 それが不可能な場合は、次の例のように、完全修飾ホスト名とIP アドレスを[!DNL /etc/hosts]に追加します。

`<ip address> <fully qualified hostname>`

## サーバーソフトウェア {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Servingには、次のサーバーソフトウェアが必要です。

**Windows**

* Microsoft®Windows Server 2008。
* 64 ビットオペレーティングシステム。

**Linux®**

* Red Hat® Enterprise 5またはCentOS 5.5以降（最新の修正パッチ付き）。
* 64 ビットオペレーティングシステム。

**メモ：** WindowsでImage Servingを使用するには、Microsoft® Visual Studio 2010をインストールする必要があります。
