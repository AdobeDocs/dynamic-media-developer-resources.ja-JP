---
title: IR 3.x 互換モジュールの設定と設定
description: IR 3.x 互換モジュールを設定して設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# IR 3.x 互換モジュールの設定と設定{#setup-and-configure-ir-x-compatibility-module}

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. ImageServer Webapps ディレクトリに移動します。
1. の内容をコピーします。 [!DNL ir] ディレクトリを [!DNL `ROOT`] ディレクトリ。
1. 開く [!DNL `ROOT/WEB-INF/web.xml`] をクリックします。
1. 行を検索 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. コメントを解除 `<servlet>` および `<servlet-mapping>` タグ。
1. 再起動 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux®の例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

次に、 [!DNL `web.xml`] お気に入りのエディターを使用して、コメントを解除します。 `<servlet>` および `<servlet-mapping>` タグ。

**Windows の例**

エクスプローラーを開き、に移動します。 `C:\Program Files\Scene7\ImageServing\webapps\ir`.

すべてのファイルとフォルダーを選択し、それらを内部にコピーする `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

次に、ファイルを編集します `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`、コメントを付けない `<servlet>` および `<servlet-mapping>` タグ。
