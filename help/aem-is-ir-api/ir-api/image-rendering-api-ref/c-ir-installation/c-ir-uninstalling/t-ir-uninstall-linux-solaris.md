---
title: Linux® および Solaris™ でのアンインストール
description: Linux® または Solaris™ システムで画像レンダリングをアンインストールするには、次の手順に従います。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# Linux® および Solaris™ でのアンインストール{#uninstalling-on-linux-and-solaris}

Linux® または Solaris™ システムで画像レンダリングをアンインストールするには、次の手順に従います。 使用できる方法は 2 つあります。 次のいずれかの操作を行います。

## 方法 1

1. [!DNL uninstall.sh] を検索します。

   これは、ImageRendering がインストールされたディレクトリにあります。 このディレクトリが削除されている場合は、元のインストールパッケージを解凍して抽出する必要 [!DNL uninstall.sh] あります。
1. [!DNL uninstall.sh] を実行し、画面の指示に従います。

## 方法 2

1. 次の操作を行って、ImageRendering を停止します。

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. システムから ImageRendering を削除します。 使用するコマンドは、システムによって異なります。
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. 手順 2 で削除されなかったディレクトリまたはファイルをすべて削除します。

