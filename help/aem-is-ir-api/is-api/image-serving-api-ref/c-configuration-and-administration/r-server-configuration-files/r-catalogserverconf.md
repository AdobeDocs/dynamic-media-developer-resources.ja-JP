---
description: 画像カタログの管理に関する設定が含まれます。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

画像カタログの管理に関する設定が含まれます。

このファイルは、JAVAプロパティファイルです。 適切な規則に従うように注意しなければならない。そうしないと、Platform Serverの起動に失敗する場合があります。 Windowsのファイルパスでは、バックスラッシュ(\)の代わりに、バックスラッシュ(\\)を二重に、またはスラッシュ(/)を1つ使用します。 このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されます。

このファイルに対する変更は、ファイルが保存された直後に有効になります。

[!DNL catalog-service.conf]では、以下に示す設定のみを変更できます。 特定の設定がない場合は、ファイルの任意の場所に追加できます。 各設定のインスタンスは1つだけ存在します。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
