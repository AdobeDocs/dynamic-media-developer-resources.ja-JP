---
description: 画像レンダリングの設定は、プラットフォームサーバの設定ファイルに保存されます。
seo-description: 画像レンダリングの設定は、プラットフォームサーバの設定ファイルに保存されます。
seo-title: 設定ファイル
solution: Experience Manager
title: 設定ファイル
topic: Scene7 Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# 設定ファイル{#configuration-files}

画像レンダリングの設定は、プラットフォームサーバの設定ファイルに保存されます。

プラットフォームサーバー構成ファイルは[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]にあります。 このファイルはJAVAプロパティファイルです。 適切な規則に従うように注意する必要があります。そうしないと、プラットフォームサーバーの開始に失敗します。 Windowsのファイルパスでは、重複のバックスラッシュ(`\\`)または1つのフォワードスラッシュ(/)を使用する必要があります。このタイプのファイルでは、バックスラッシュがエスケープ文字として使用されるからです。 ファイルにドキュメントに記載されていないプロパティが含まれていますが、これは内部サーバーでの使用を目的としており、変更しないでください。

すべての画像レンダ [リング設定のリストについては](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) 、『設定リファレンス』を参照してください。
