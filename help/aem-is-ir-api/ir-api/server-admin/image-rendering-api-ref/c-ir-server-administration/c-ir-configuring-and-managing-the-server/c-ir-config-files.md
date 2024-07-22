---
description: 画像レンダリングの設定は、設定ファイル  [!DNL Platform Server]  保存されます。
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

画像レンダリングの設定は、[!DNL Platform Server] 設定ファイルに保存されています。

プラットフォーム サーバー構成ファイルは [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf] にあります。 このファイルは JAVA プロパティファイルです。 適切な規則に従うように注意する必要があります。そうしないと、[!DNL Platform Server] ークフローが開始されない場合があります。 Windows のファイル・パスでは、単純なバックスラッシュ（\）ではなく、2 つのバックスラッシュ（`\\`）または 1 つのスラッシュ（/）を使用する必要があります。これは、このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されるためです。 このファイルには、ドキュメントに記載されていないプロパティが含まれています。これらのプロパティは内部サーバーで使用するためのものであり、変更しないでください。

すべての画像レンダリング設定のリストについては、[ 設定リファレンス ](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) を参照してください。
