---
description: 画像カタログには、フォント、ICCプロファイル、コマンドマクロに加え、多くのサーバ設定が用意されています。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# 画像カタログ{#image-catalogs}

画像カタログには、フォント、ICCプロファイル、コマンドマクロに加え、多くのサーバ設定が用意されています。

要求で使用される画像IDと静的コンテンツIDを実際のファイルパスにマッピングし、画像マップなどの様々な画像メタデータを保存し、テンプレートと画像セットのコンテナを提供します。

画像カタログは、Platform Serverのみがアクセスし、Image Serverはアクセスしません。 カタログ属性ファイルには.iniサフィックスが必要で、プラットフォームサーバーのカタログフォルダ(`PS::CatalogFolder`)に配置します。 少なくともデフォルトの画像カタログが必要です。プラットフォームサーバーを正しく機能させるには、すべての属性を指定する必要があります。
