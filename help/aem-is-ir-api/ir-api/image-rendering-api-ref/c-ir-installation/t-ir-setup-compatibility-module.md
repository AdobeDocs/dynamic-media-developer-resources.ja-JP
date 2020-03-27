---
description: IR 3.x互換モジュールを設定し、設定する必要があります。
seo-description: IR 3.x互換モジュールを設定し、設定する必要があります。
seo-title: IR 3.x互換モジュールのセットアップと設定
solution: Experience Manager
title: IR 3.x互換モジュールのセットアップと設定
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IR 3.x互換モジュールのセットアップと設定{#setup-and-configure-ir-x-compatibility-module}

IR 3.x互換モジュールを設定し、設定する必要があります。

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. ImageServer Webappsディレクトリに移動します。
1. ディレクトリの内容をディレ [!DNL ir] クトリにコピー [!DNL ROOT] します。
1. テキスト [!DNL ROOT/WEB-INF/web.xml] エディターで開きます。
1. 行の検索 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. タグとタグのコメ `<servlet>` ントを解 `<servlet-mapping>` 除します。
1. Restart `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
>**Linuxの例**
>
>`cd /usr/local/scene7/ImageServing/webapps/ROOT`
>
>`cp -r ../ir/* ./`
>
>`cd WEB-INF`
>
>次に、お気に入 [!DNL web.xml]りのエディターを使用してタグとタグのコメ `<servlet>` ントを解除 `<servlet-mapping>` します。
>
>**Windowsの例**
>
>エクスプローラを開き、に移動しま [!DNL C:\Program Files\Scene7\ImageServing\webapps\ir]す。
>
>すべてのファイルとフォルダーを選択し、内部にコピーしま [!DNL C:\Program Files\Scene7\ImageServing\webapps\ROOT]す。
>
>次に、タグとタグのコ [!DNL c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml]メントを解除して、フ `<servlet>` ァイルを編 `<servlet-mapping>` 集します。

