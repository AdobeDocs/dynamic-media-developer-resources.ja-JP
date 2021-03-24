---
description: 画像レンダリングの設定は、プラットフォームサーバーの設定ファイルに保存されます。
solution: Experience Manager
title: 設定ファイル
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# 構成ファイル{#configuration-files}

画像レンダリングの設定は、プラットフォームサーバーの設定ファイルに保存されます。

プラットフォームサーバー構成ファイルは、[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]にあります。 このファイルはJAVAプロパティファイルです。 適切な規則に従うように注意する必要があります。規則に従わないと、プラットフォームサーバーの開始に失敗する場合があります。 Windowsのファイルパスでは、重複のバックスラッシュ(`\\`)または1つのスラッシュ(/)を、単純なバックスラッシュ(\)の代わりに使用する必要があります。これは、このタイプのファイルではバックスラッシュがエスケープ文字として使用されるためです。 ファイルにドキュメントに記載されていないプロパティが含まれていますが、これは内部サーバーでの使用を目的としており、変更しないでください。

すべてのイメージレンダリング設定のリストについては、『Configuration Settings Reference](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)』を参照してください。[
