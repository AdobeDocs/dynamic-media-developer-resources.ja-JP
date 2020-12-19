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
workflow-type: tm+mt
source-wordcount: '138'
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



