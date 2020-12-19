---
description: IR 3.x互換モジュールをセットアップし、構成する必要があります。
seo-description: IR 3.x互換モジュールをセットアップし、構成する必要があります。
seo-title: IR 3.x互換モジュールのセットアップと構成
solution: Experience Manager
title: IR 3.x互換モジュールのセットアップと構成
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# IR 3.x互換モジュール{#setup-and-configure-ir-x-compatibility-module}のセットアップと設定

IR 3.x互換モジュールをセットアップし、構成する必要があります。

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. ImageServer Webappsディレクトリに移動します。
1. [!DNL ir]ディレクトリの内容を[!DNL ROOT]ディレクトリにコピーします。
1. テキストエディターで[!DNL ROOT/WEB-INF/web.xml]を開きます。
1. `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`行を探します
1. `<servlet>`タグと`<servlet-mapping>`タグのコメントを解除します。
1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`を再起動します。

**Linuxの例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

次に、お気に入りのエディターを使って[!DNL web.xml]を編集し、`<servlet>`タグと`<servlet-mapping>`タグのコメントを解除します。

**Windowsの例**

エクスプローラを開き、`C:\Program Files\Scene7\ImageServing\webapps\ir`に移動します。

すべてのファイルとフォルダーを選択し、`C:\Program Files\Scene7\ImageServing\webapps\ROOT`内にコピーします。

次に、ファイル`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`を編集し、`<servlet>`タグと`<servlet-mapping>`タグのコメントを解除します。
