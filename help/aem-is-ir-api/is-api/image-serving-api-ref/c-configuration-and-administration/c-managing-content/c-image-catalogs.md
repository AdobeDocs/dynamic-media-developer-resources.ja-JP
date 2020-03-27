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

---


# 画像カタログ{#image-catalogs}

画像カタログには、フォント、ICCプロファイル、コマンドマクロに加え、多くのサーバ設定が用意されています。

要求で使用される画像IDと静的コンテンツIDを実際のファイルパスにマッピングし、画像マップなどの様々な画像メタデータを保存し、テンプレートと画像セットのコンテナを提供します。

画像カタログは、Platform Serverによってのみアクセスされ、Image Serverによってはアクセスされません。 カタログ属性ファイルは.iniサフィックスを持ち、プラットフォームサーバのカタログフォルダ( `PS::CatalogFolder`)に配置する必要があります。 少なくともデフォルトの画像カタログが必要で、プラットフォームサーバを正しく機能させるためには、すべての属性を設定する必要があります。
