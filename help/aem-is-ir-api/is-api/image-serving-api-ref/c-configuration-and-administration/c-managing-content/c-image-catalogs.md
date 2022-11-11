---
description: 画像カタログには、多くのサーバ設定に加え、フォント、ICC プロファイル、コマンドマクロが含まれます。
solution: Experience Manager
title: 画像カタログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 画像カタログ{#image-catalogs}

画像カタログには、多くのサーバ設定に加え、フォント、ICC プロファイル、コマンドマクロが含まれます。

リクエストで使用される画像および静的コンテンツ ID を実際のファイルパスにマッピングし、画像マップなどの様々な画像メタデータを保存し、テンプレートおよび画像セットのコンテナを提供します。

画像カタログには、 [!DNL Platform Server]Image Server では取得できません。 カタログ属性ファイルは.ini サフィックスを持ち、 [!DNL Platform Server]のカタログフォルダ ( `PS::CatalogFolder`) をクリックします。 少なくともデフォルトの画像カタログが必要です。を正しく機能させるには、すべての属性を設定する必要があります。 [!DNL Platform Server].
