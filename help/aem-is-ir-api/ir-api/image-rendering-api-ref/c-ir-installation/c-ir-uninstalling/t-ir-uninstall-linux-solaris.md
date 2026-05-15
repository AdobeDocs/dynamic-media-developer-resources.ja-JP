---
title: Linux®およびSolarisでのアンインストール™
description: Linux®またはSolaris™ システムでImage Renderingをアンインストールするには、次の手順に従います。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# Linux®およびSolarisでのアンインストール™{#uninstalling-on-linux-and-solaris}

Linux®またはSolaris™ システムでImage Renderingをアンインストールするには、次の手順に従います。 使用できる方法は2つあります。 次のいずれかの操作を行います。

## 方法1

1. [!DNL uninstall.sh]を検索します。

   ImageRenderingがインストールされたディレクトリにあります。 このディレクトリが削除された場合は、元のインストールパッケージを解凍して解凍し、[!DNL uninstall.sh]を抽出する必要があります。
1. [!DNL uninstall.sh]を実行し、画面の指示に従います。

## 方法2

1. 次の操作でImageRenderingを停止します。

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. システムからImageRenderingを削除します。 使用するコマンドは、システムによって異なります。
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. 手順2で削除されなかったディレクトリまたはファイルを削除します。

