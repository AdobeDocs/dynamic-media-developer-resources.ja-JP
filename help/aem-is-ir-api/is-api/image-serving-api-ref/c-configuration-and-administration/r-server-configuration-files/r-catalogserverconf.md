---
description: 画像カタログの管理に関する設定が含まれます。
seo-description: 画像カタログの管理に関する設定が含まれます。
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# catalog-server.conf{#catalog-server-conf}

画像カタログの管理に関する設定が含まれます。

このファイルはJAVAプロパティファイルです。 適切な規則に従うように注意しなければならない。そうしないと、プラットフォームサーバーの起動に失敗する可能性があります。 Windowsファイルパスでは、バックスラッシュ「\」の代わりに、二重のバックスラッシュ「\\」または単一のスラッシュ「/」を使用します。 バックスラッシュは、このタイプのファイルではエスケープ文字として使用されます。

このファイルに対する変更は、ファイルが保存された直後に有効になります。

で変更できるのは、次に示す設定のみで [!DNL catalog-service.conf]す。 特定の設定がない場合は、ファイル内の任意の場所に追加できます。 各設定のインスタンスは1つだけ存在できます。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
