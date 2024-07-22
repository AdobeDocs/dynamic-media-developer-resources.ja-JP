---
title: IR 3.x 互換モジュールのセットアップと設定
description: IR 3.x 互換モジュールをセットアップして設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# IR 3.x 互換モジュールのセットアップと設定{#setup-and-configure-ir-x-compatibility-module}

1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` を停止。
1. ImageServer webapps ディレクトリに移動します。
1. [!DNL ir] ディレクトリの内容を [!DNL `ROOT`] ディレクトリにコピーします。
1. [!DNL `ROOT/WEB-INF/web.xml`] をテキストエディターで開きます。
1. 行 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->` を検索
1. `<servlet>` タグと `<servlet-mapping>` タグのコメントを解除します。
1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` を再起動します。

**Linux® の例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

次に、お気に入りのエディターを使用して [!DNL `web.xml`] を編集し、`<servlet>` タグと `<servlet-mapping>` タグのコメントを解除します。

**Windows の例**

エクスプローラーを開き、`C:\Program Files\Scene7\ImageServing\webapps\ir` に移動します。

すべてのファイルとフォルダーを選択し、`C:\Program Files\Scene7\ImageServing\webapps\ROOT` 内にコピーします。

次に、ファイル `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` を編集し、`<servlet>` タグと `<servlet-mapping>` タグのコメントを解除します。
