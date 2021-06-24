---
description: 画像カタログは、画像に関する情報とサポートデータ（フォントやICCプロファイルなど）をサーバーに提供するために使用されます。
solution: Experience Manager
title: 概要
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 概要{#overview}

画像カタログは、画像に関する情報とサポートデータ（フォントやICCプロファイルなど）をサーバーに提供するために使用されます。

画像カタログは、画像に関する情報とサポートデータ（フォントやICCプロファイルなど）をサーバーに提供するために使用されます。

各画像カタログは、必須のカタログ属性ファイルと、オプションのカタログデータファイルのセットで構成されます。

* 画像データファイル。画像とテンプレート、およびそれらに関連付けられたメタデータを定義します。
* SVGデータファイル。SVGファイルと、それに関連するメタデータの項目を定義します。
* リクエストマクロの定義を提供するマクロ定義ファイル。
* テキストフォントを追跡するフォントマップファイル。
* ICCカラープロファイルを定義するプロファイルマップファイル。
* HTTPリクエストの前処理ルールを定義するルールセットファイル。

カタログデータファイルは、カタログ属性ファイル内のファイル参照によって画像カタログに関連付けられます。 同じカタログデータファイルを複数の画像カタログで共有できます。

カタログ属性ファイルには、[!DNL .ini]ファイルサフィックスが付き、Platform Serverのカタログフォルダー(`PlatformServer::catalog.rootPath`)に存在する必要があります。 カタログデータファイルは、同じフォルダーまたはPlatform Serverがアクセスできる他のフォルダーに配置できます。

このドキュメントでは、Dynamic Media Image Servingシステムの画像カタログファイル形式について説明します。 対象となるオーディエンスは、WebまたはカスタムアプリケーションでDynamic Media Image Servingを活用したい経験豊富なプログラマーやWebサイト開発者です。

読者は、Dynamic Media Image Servingシステム、一般的なHTTPプロトコル標準および規則、基本的な画像用語に一般に精通していることを前提としています。
