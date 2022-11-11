---
description: 画像レンダリングの設定は、 [!DNL Platform Server] 設定ファイル。
solution: Experience Manager
title: 設定ファイル
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 設定ファイル{#configuration-files}

画像レンダリングの設定は、 [!DNL Platform Server] 設定ファイル。

プラットフォームサーバー設定ファイルは、[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf] を参照してください。 このファイルは、JAVA プロパティファイルです。 適切な規則に従うように注意する必要があります。そうでない場合、 [!DNL Platform Server] を起動できない可能性があります。 二重のバックスラッシュ (`\\`) または Windows のファイルパスでは、単純なバックスラッシュ (\) の代わりに 1 つのスラッシュ (/) を使用する必要があります。これは、このタイプのファイルではバックスラッシュがエスケープ文字として使用されるからです。 ファイルには、ドキュメントに記載されていないプロパティが含まれています。このプロパティは内部サーバーでの使用に使用され、変更することはできません。

詳しくは、 [設定リファレンス](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) を参照してください。
