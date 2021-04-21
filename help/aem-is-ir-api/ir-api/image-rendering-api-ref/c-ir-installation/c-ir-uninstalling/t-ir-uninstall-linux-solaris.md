---
description: LinuxまたはSolarisシステムでイメージレンダリングをアンインストールするには、次の手順に従います。
solution: Experience Manager
title: LinuxおよびSolarisでのアンインストール
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# LinuxおよびSolarisでのアンインストール{#uninstalling-on-linux-and-solaris}

LinuxまたはSolarisシステムでイメージレンダリングをアンインストールするには、次の手順に従います。

LinuxまたはSolarisシステムでイメージレンダリングをアンインストールするには、2つの方法があります。

**方法1**

1. 検索 [!DNL uninstall.sh].

   このディレクトリは、ImageRenderingのインストール元のディレクトリにあります。 このディレクトリが削除された場合、[!DNL uninstall.sh]を抽出するには、元のインストールパッケージを圧縮解除し、転送を解除する必要があります。
1. [!DNL uninstall.sh]を実行し、画面の指示に従います。

>**方法2**
>
>1. ImageRenderingを停止する時間：` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. システムからImageRenderingを削除します。

>
>   
ImageRenderingを削除するコマンドは、使用しているシステムによって異なります。
>
>   Linux:`rpm -e ImageRendering`
>
>   Solaris:`pkgrm ImageRendering`
>
>1. 手順2で削除しなかったディレクトリまたはファイルを削除します。

>



