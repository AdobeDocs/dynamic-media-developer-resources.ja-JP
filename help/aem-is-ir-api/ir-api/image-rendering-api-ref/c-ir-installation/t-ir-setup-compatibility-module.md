---
title: IR 3.x互換モジュールのセットアップと設定
description: IR 3.x互換モジュールをセットアップして設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 0%

---

# IR 3.x互換モジュールのセットアップと設定{#setup-and-configure-ir-x-compatibility-module}

1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`を停止します。
1. ImageServer web apps ディレクトリに移動します。
1. [!DNL ir] ディレクトリの内容を[!DNL `ROOT`] ディレクトリにコピーします。
1. [!DNL `ROOT/WEB-INF/web.xml`]をテキストエディターで開きます。
1. `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`行を検索
1. タグ `<servlet>`と`<servlet-mapping>`のコメントを解除します。
1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`を再起動します。

**Linux®例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

次に、お気に入りのエディターを使用して[!DNL `web.xml`]を編集し、`<servlet>`および`<servlet-mapping>` タグのコメントを解除します。

**Windowsの例**

エクスプローラーを開き、`C:\Program Files\Scene7\ImageServing\webapps\ir`に移動します。

すべてのファイルとフォルダーを選択し、`C:\Program Files\Scene7\ImageServing\webapps\ROOT`内のファイルとフォルダーをコピーします。

次に、ファイル `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`を編集し、`<servlet>`および`<servlet-mapping>` タグのコメントを解除します。

