---
description: これは、 [!DNL Platform Server]. 画像レンダリングが有効な場合、はアクセスログデータを同じファイルに書き込みます。
solution: Experience Manager
title: アクセスログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# アクセスログ{#access-log}

これは、 [!DNL Platform Server]. 画像レンダリングが有効な場合、はアクセスログデータを同じファイルに書き込みます。

アクセスログは server.xml で設定します。

>[!NOTE]
>
>画像サービング用のクライアントトラフィック ( [!DNL /is/image/*]) および画像レンダリング ( [!DNL /ir/render/*]) の場合、アクセスログには、特定の内部トラフィックが含まれる場合があります。へのアクセス [!DNL Platform Server] カタログシステム ( [!DNL /is-catalog/*])、キャッシュの共有およびエラーのリダイレクトリクエスト ( [!DNL /is/cache/*])、にデプロイされた他のパッケージへのアクセス [!DNL Platform Server]例えば、Dynamic Media Viewers ( [!DNL /is-viewers/*])、静的トラフィックおよび静的コンテンツのリクエストが、 [!DNL Platform Server] ( 例： [!DNL /is-docs/*]) をクリックします。

次を含むリクエスト： [!DNL /is-catalog] および [!DNL /is/cache] ルートパスは、常にクライアントトラフィック分析から除外する必要があります。
