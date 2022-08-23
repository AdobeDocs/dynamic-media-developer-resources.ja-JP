---
title: Linux®および Solaris™でのアンインストール
description: 次の手順に従って、Linux®または Solaris™システムで Image Rendering をアンインストールします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# Linux®および Solaris™でのアンインストール{#uninstalling-on-linux-and-solaris}

次の手順に従って、Linux®または Solaris™システムで Image Rendering をアンインストールします。 使用できる方法は 2 つあります。 次のいずれかの操作を行います。

## 方法 1

1. 検索 [!DNL uninstall.sh].

   ImageRendering がインストールされたディレクトリにあります。 このディレクトリが削除された場合は、元のインストールパッケージを非圧縮にし、抽出するために未保存にする必要があります [!DNL uninstall.sh].
1. 実行 [!DNL uninstall.sh] 画面に表示される指示に従います。

## 方法 2

1. 次の設定で ImageRendering を停止します。

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. システムから ImageRendering を削除します。 使用するコマンドは、システムによって異なります。
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. 手順 2 で削除しなかったディレクトリやファイルを削除します。

