---
description: LinuxまたはSolarisシステムでImage Renderingをアンインストールするには、次の手順に従います。
solution: Experience Manager
title: LinuxおよびSolarisでのアンインストール
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# LinuxおよびSolarisでのアンインストール{#uninstalling-on-linux-and-solaris}

LinuxまたはSolarisシステムでImage Renderingをアンインストールするには、次の手順に従います。

LinuxまたはSolarisシステムでImage Renderingをアンインストールする方法は2つあります。

**方法1**

1. 検索 [!DNL uninstall.sh].

   ImageRenderingのインストール元のディレクトリにあります。 このディレクトリが削除された場合は、元のインストールパッケージを解凍し、解凍して[!DNL uninstall.sh]を抽出する必要があります。
1. [!DNL uninstall.sh]を実行し、画面の指示に従います。

>**方法2**
>
>1. ImageRenderingを停止します。` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. システムからImageRenderingを削除します。

>
>   
ImageRenderingを削除するコマンドは、システムによって異なります。
>
>   Linux:`rpm -e ImageRendering`
>
>   Solaris:`pkgrm ImageRendering`
>
>1. 手順2で削除しなかったディレクトリやファイルを削除します。

>


