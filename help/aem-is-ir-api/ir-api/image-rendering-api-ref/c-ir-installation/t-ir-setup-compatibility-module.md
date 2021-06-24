---
description: IR 3.x互換モジュールを設定し、設定する必要があります。
solution: Experience Manager
title: IR 3.x互換モジュールのセットアップと設定
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# IR 3.x互換モジュールのセットアップと設定{#setup-and-configure-ir-x-compatibility-module}

IR 3.x互換モジュールを設定し、設定する必要があります。

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. ImageServer Webアプリディレクトリに移動します。
1. [!DNL ir]ディレクトリの内容を[!DNL ROOT]ディレクトリにコピーします。
1. テキストエディターで[!DNL ROOT/WEB-INF/web.xml]を開きます。
1. 行`<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`を検索します。
1. `<servlet>`タグと`<servlet-mapping>`タグのコメントを解除します。
1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`を再起動します。

**Linuxの例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

次に、お気に入りのエディターを使用して[!DNL web.xml]を編集し、`<servlet>`タグと`<servlet-mapping>`タグのコメントを解除します。

**Windowsの例**

エクスプローラーを開き、`C:\Program Files\Scene7\ImageServing\webapps\ir`に移動します。

すべてのファイルとフォルダーを選択し、`C:\Program Files\Scene7\ImageServing\webapps\ROOT`内にコピーします。

次に、ファイル`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`を編集し、`<servlet>`タグと`<servlet-mapping>`タグのコメントを解除します。
