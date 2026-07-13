---
description: このドキュメントでは、Dynamic Media画像レンダリングサーバーの管理方法について説明します。
solution: Experience Manager
title: サーバー管理の概要
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: 'https://experienceleague.adobe.com/t9zGehwMxhHq1HrP3mmNGvkthmqYxX2ijeyihn5OEWI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# サーバー管理の概要{#server-administration-overview}

このドキュメントでは、Dynamic Media画像レンダリングサーバーの管理方法について説明します。

画像レンダリングは、次の2つの主要コンポーネントで構成されています。

* Java パッケージがImage Serving [!DNL Platform Server]と共にデプロイされ、クライアント接続、キャッシュ、マテリアルカタログを管理します。
* ネイティブコードモジュールは、Image Serverの拡張ライブラリとしてデプロイされ、主要な画像レンダリング機能を実装します。

両方のコンポーネントは総称して&#x200B;*レンダーサーバー*&#x200B;と呼ばれます。

画像レンダリングは、多くのサーバー機能を画像サービングと共有し、すべてのオプションは設定ファイルを編集することによって設定されます。 追加の構成属性は、デフォルトカタログ（[!DNL default.ini]）または特定のマテリアルカタログによって提供されます。 詳しくは、マテリアルカタログを参照してください。

画像レンダリングのインストールフォルダー（*[!DNL install_folder]*）は[!DNL *[!DNL install_root]*/ImageRendering]です。 Windowsでは、デフォルトの&#x200B;*[!DNL install_root]*&#x200B;は`C:\Program Files\Scene7`です。 インストール時に別のフォルダーを指定できます。 Linuxでは、*[!DNL install_root]*&#x200B;は常に[!DNL /usr/local/scene7]である必要があります。 シンボリックリンクを使用できます。

すべてのファイルパスは、UNIXでは大文字と小文字を区別し、Windowsでは大文字と小文字を区別しません。

