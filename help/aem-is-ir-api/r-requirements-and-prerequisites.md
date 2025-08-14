---
title: システム要件および前提条件
description: Dynamic Media 画像サービングを使用する前に、お使いのシステムがシステム要件を満たしていることを確認してください。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# システム要件および前提条件{#system-requirements-and-prerequisites}

Dynamic Media 画像サービングを使用する前に、お使いのシステムがシステム要件を満たしていることを確認してください。

## サーバハードウェア {#section-f3c14a7bc1b745118602659628df779f}

サーバーは次のハードウェア要件を満たしている必要があります。

>[!NOTE]
>
>AMD64 および Intel® EM64T を搭載したプロセッサを搭載したシステムは、通常、NUMA （Non-Uniform Memory Architecture）プラットフォームとして設定されます。 つまり、カーネルは、単一のメモリノードを構築するのではなく、ブート時に複数のメモリノードを構築します。 複数のノード構成体を使用すると、他のノードが消費される前に、1 つ以上のノードでメモリが枯渇する可能性があります。 メモリ不足が発生すると、使用可能なメモリがあるにもかかわらず、カーネルはプロセス（Image Server や [!DNL Platform Server] など）を強制終了する可能性があります。 そのため、Adobeでは、このようなシステムを実行する場合は、NUMA をオフにすることをお勧めします。 `numa=off` start オプションを使用して、カーネルがこれらのプロセスを停止するのを避けます。

**Windows**

* 4 コア以上の Intel Xeon® または AMD® Opteron CPU
* 1 GB 以上の RAM
* スワップ領域は、物理メモリ（RAM）の少なくとも 2 倍の量に等しくなります。
* インストールと基本操作に 2 GB のハードディスク空き容量が必要です。ソースイメージ、ログ、データキャッシュ、マニフェストファイル用に、さらにディスク容量が必要です。
* ファースト イーサネット ネットワーク インターフェイス カード。

**Linux®**

* 4 コア以上の Intel Xeon® または AMD® Opteron CPU
* 16 GB 以上の RAM。
* スワップが無効です（推奨）。
* インストールと基本操作に 2 GB のハードディスク空き容量が必要です。ソースイメージ、ログ、データキャッシュ、マニフェストファイル用に、さらにディスク容量が必要です。
* ファースト イーサネット ネットワーク インターフェイス カード。

**注意（Linux®）:** SELinux がオンの場合、画像サービングは機能しません。 このオプションはデフォルトで有効になっています。 SELinux を無効にするには、[!DNL /etc/selinux/config] ファイルを編集し、SELinux 値を次の値から変更します。

`SELINUX=enforcing`

終了

`SELINUX=disabled`

**注意（Linux®）:** サーバーのホスト名が IP アドレスに解決できることを確認してください。 解決できない場合は、次の例のように、完全修飾ホスト名と IP アドレスを [!DNL /etc/hosts] に追加してください。

`<ip address> <fully qualified hostname>`

## サーバーソフトウェア {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media 画像サービングには、次のサーバーソフトウェアが必要です。

**Windows**

* Microsoft®Windows Server 2008。
* 64 ビットオペレーティングシステム。

**Linux®**

* 最新の修正パッチが適用された Red Hat® Enterprise 5 または CentOS 5.5 以降。
* 64 ビットオペレーティングシステム。

**注意：** Windows で画像サービングを使用するには、Microsoft® Visual Studio 2010 をインストールする必要があります。
