---
description: 画像カタログの管理に関する設定が含まれます。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

画像カタログの管理に関する設定が含まれます。

このファイルは、JAVA プロパティファイルです。 適切な規則に従うように注意しなければならない。それ以外の場合は [!DNL Platform Server] を開始できない可能性があります。 Windows のファイルパスでは、バックスラッシュ「\」の代わりに、バックスラッシュ「\」またはスラッシュ「/」を 1 つ使用します。 このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されます。

このファイルに対する変更は、ファイルが保存された直後に有効になります。

以下に示す設定のみを [!DNL catalog-service.conf]. 特定の設定がない場合は、ファイルの任意の場所に追加できます。 各設定のインスタンスは 1 つだけ存在します。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
