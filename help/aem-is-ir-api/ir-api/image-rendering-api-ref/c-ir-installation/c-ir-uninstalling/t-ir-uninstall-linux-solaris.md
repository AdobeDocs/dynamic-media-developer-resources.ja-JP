---
description: LinuxまたはSolarisシステムでイメージレンダリングをアンインストールするには、次の手順に従います。
seo-description: LinuxまたはSolarisシステムでイメージレンダリングをアンインストールするには、次の手順に従います。
seo-title: LinuxおよびSolarisでのアンインストール
solution: Experience Manager
title: LinuxおよびSolarisでのアンインストール
topic: Scene7 Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LinuxおよびSolarisでのアンインストール{#uninstalling-on-linux-and-solaris}

LinuxまたはSolarisシステムでイメージレンダリングをアンインストールするには、次の手順に従います。

LinuxまたはSolarisシステムでイメージレンダリングをアンインストールする方法は2つあります。

**方法1**

1. 検索 [!DNL uninstall.sh].

   ImageRenderingのインストール元のディレクトリ内にあります。 このディレクトリが削除された場合は、元のインストールパッケージを圧縮解除し、展開する必要がありま [!DNL uninstall.sh]す。
1. を実行 [!DNL uninstall.sh] し、画面の指示に従います。
>**方法2**
>
>1. 次を使用してImageRenderingを停止： ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. システムからImageRenderingを削除します。
>
>   
ImageRenderingを削除するコマンドは、使用しているシステムによって異なります。
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. 手順2で削除されなかったディレクトリまたはファイルを削除します。
>



