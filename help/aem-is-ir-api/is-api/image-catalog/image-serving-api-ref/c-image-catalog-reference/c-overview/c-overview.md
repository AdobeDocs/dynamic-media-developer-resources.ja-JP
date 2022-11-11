---
description: 画像カタログは、画像に関する情報とサポートデータ（フォントや ICC プロファイルなど）をサーバに提供するために使用されます。
solution: Experience Manager
title: 概要
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# 概要{#overview}

画像カタログは、画像に関する情報とサポートデータ（フォントや ICC プロファイルなど）をサーバに提供するために使用されます。

画像カタログは、画像に関する情報とサポートデータ（フォントや ICC プロファイルなど）をサーバに提供するために使用されます。

各画像カタログは、必須のカタログ属性ファイルと、オプションのカタログデータファイルのセットで構成されます。

* 画像データファイル。画像とテンプレート、およびそれに関連するメタデータを定義します。
* SVGデータファイル。SVGファイルと、関連するメタデータを定義します。
* マクロ定義ファイル。リクエストマクロの定義を提供します。
* テキストフォントを追跡するフォントマップファイル。
* プロファイルマップファイル。ICC カラープロファイルを定義します。
* HTTP リクエストの前処理ルールを定義するルールセットファイル。

カタログデータファイルは、カタログ属性ファイル内のファイル参照によって画像カタログに関連付けられます。 同じカタログデータファイルを複数の画像カタログで共有できます。

カタログ属性ファイルには [!DNL .ini] ファイルサフィックスとは、 [!DNL Platform Server]のカタログフォルダ ( `PlatformServer::catalog.rootPath`) をクリックします。 カタログデータファイルは、同じフォルダー内、または [!DNL Platform Server].

このドキュメントでは、Dynamic Media Image Serving システムの画像カタログファイル形式について説明します。 対象となるオーディエンスは、Web またはカスタムアプリケーションでDynamic Media Image Serving を利用する、経験豊富なプログラマーや Web サイト開発者です。

読者は、Dynamic Media Image Serving システム、一般的な HTTP プロトコルの標準と規則、基本的な画像の用語に一般に精通していることを前提としています。
