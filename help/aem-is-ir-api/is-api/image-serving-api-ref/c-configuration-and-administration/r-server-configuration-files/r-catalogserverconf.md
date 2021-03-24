---
description: 画像カタログの管理に関する設定が含まれます。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

画像カタログの管理に関する設定が含まれます。

このファイルはJAVAプロパティファイルです。 適切な規則に従うように注意しなければならない。そうしないと、Platform Serverが開始に失敗する場合があります。 Windowsのファイルパスでは、重複のバックスラッシュ「\\」を使用するか、バックスラッシュの代わりに1つのスラッシュ(/)を使用します。 このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されます。

このファイルに対する変更は、ファイルが保存された後すぐに有効になります。

[!DNL catalog-service.conf]では、次の設定のみを変更できます。 特定の設定がない場合は、ファイル内の任意の場所に追加できます。 各設定のインスタンスは1つだけ存在します。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
