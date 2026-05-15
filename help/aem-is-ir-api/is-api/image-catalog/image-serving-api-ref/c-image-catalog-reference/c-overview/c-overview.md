---
description: 画像カタログは、画像とサポートデータ（フォントやICC プロファイルなど）に関する情報をサーバーに提供するために使用されます。
solution: Experience Manager
title: 概要
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
TQID: 'https://experienceleague.adobe.com/RFHaFaMFjOo2Igk-pQRXrQSCtSMmVCWarO6wu0mv4g8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 概要{#overview}

画像カタログは、画像とサポートデータ（フォントやICC プロファイルなど）に関する情報をサーバーに提供するために使用されます。

画像カタログは、画像とサポートデータ（フォントやICC プロファイルなど）に関する情報をサーバーに提供するために使用されます。

各画像カタログは、必要なカタログ属性ファイルとオプションのカタログデータファイルのセットで構成されます。

* 画像データファイル。画像とテンプレート、および関連するメタデータを列挙します。
* SVG データファイル。SVG ファイルとその関連メタデータを列挙します。
* マクロ定義ファイル。リクエストマクロの定義を提供します。
* フォントマップファイル。テキストフォントを追跡します。
* ICC カラープロファイルを列挙したプロファイルマップファイル。
* ルールセットファイル。HTTP リクエストの前処理ルールを定義します。

カタログデータファイルは、カタログ属性ファイル内のファイル参照によって画像カタログに関連付けられます。 同じカタログデータファイルを複数の画像カタログで共有できます。

カタログ属性ファイルには[!DNL .ini] ファイル サフィックスが必要で、[!DNL Platform Server]のカタログ フォルダー（`PlatformServer::catalog.rootPath`）に配置する必要があります。 カタログデータファイルは、同じフォルダーまたは[!DNL Platform Server]にアクセス可能な他のフォルダーに配置できます。

このドキュメントでは、Dynamic Media Image Serving システムの画像カタログファイル形式について説明します。 対象となるユーザーは、Web アプリケーションまたはカスタムアプリケーションにDynamic Media Image Servingを活用したい経験豊富なプログラマーおよびweb サイト開発者です。

読者は、Dynamic Media画像サービングシステム、一般的なHTTP プロトコルの標準と規則、および基本的な画像用語に一般的に精通していると仮定します。
