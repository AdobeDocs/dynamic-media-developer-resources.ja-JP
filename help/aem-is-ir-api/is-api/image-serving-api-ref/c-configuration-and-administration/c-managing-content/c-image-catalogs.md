---
description: 画像カタログは、多くのサーバ設定に加え、フォント、ICCプロファイル、コマンドマクロを提供します。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 画像カタログ{#image-catalogs}

画像カタログは、多くのサーバ設定に加え、フォント、ICCプロファイル、コマンドマクロを提供します。

リクエストで使用される画像と静的コンテンツIDを実際のファイルパスにマッピングし、画像マップなどの様々な画像メタデータを保存し、テンプレートと画像セットのコンテナを提供します。

画像カタログは、Platform Serverのみがアクセスし、Image Serverはアクセスしません。 カタログ属性ファイルには.iniサフィックスを付け、Platform Serverのカタログフォルダー(`PS::CatalogFolder`)に配置する必要があります。 少なくともデフォルトの画像カタログが必要です。Platform Serverを正しく機能させるには、すべての属性を設定する必要があります。
