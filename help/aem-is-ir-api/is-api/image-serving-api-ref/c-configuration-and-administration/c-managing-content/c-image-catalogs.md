---
description: 画像カタログには、フォント、ICCプロファイル、コマンドマクロに加え、多くのサーバ設定が用意されています。
seo-description: 画像カタログには、フォント、ICCプロファイル、コマンドマクロに加え、多くのサーバ設定が用意されています。
seo-title: 画像カタログ
solution: Experience Manager
title: 画像カタログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# 画像カタログ{#image-catalogs}

画像カタログには、フォント、ICCプロファイル、コマンドマクロに加え、多くのサーバ設定が用意されています。

要求で使用される画像IDと静的コンテンツIDを実際のファイルパスにマッピングし、画像マップなどの様々な画像メタデータを保存し、テンプレートと画像セットのコンテナを提供します。

画像カタログは、Platform Serverのみがアクセスし、Image Serverはアクセスしません。 カタログ属性ファイルには.iniサフィックスが必要で、プラットフォームサーバーのカタログフォルダ(`PS::CatalogFolder`)に配置します。 少なくともデフォルトの画像カタログが必要です。プラットフォームサーバーを正しく機能させるには、すべての属性を指定する必要があります。
