---
description: 画像レンダリングの設定は、プラットフォームサーバーの設定ファイルに保存されます。
seo-description: 画像レンダリングの設定は、プラットフォームサーバーの設定ファイルに保存されます。
seo-title: 設定ファイル
solution: Experience Manager
title: 設定ファイル
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# 構成ファイル{#configuration-files}

画像レンダリングの設定は、プラットフォームサーバーの設定ファイルに保存されます。

プラットフォームサーバー構成ファイルは、[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]にあります。 このファイルはJAVAプロパティファイルです。 適切な規則に従うように注意する必要があります。規則に従わないと、プラットフォームサーバーの開始に失敗する場合があります。 Windowsのファイルパスでは、重複のバックスラッシュ(`\\`)または1つのスラッシュ(/)を、単純なバックスラッシュ(\)の代わりに使用する必要があります。これは、このタイプのファイルではバックスラッシュがエスケープ文字として使用されるためです。 ファイルにドキュメントに記載されていないプロパティが含まれていますが、これは内部サーバーでの使用を目的としており、変更しないでください。

すべてのイメージレンダリング設定のリストについては、『Configuration Settings Reference](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)』を参照してください。[
