---
description: 画像レンダリングの設定は、Platform Serverの設定ファイルに保存されます。
solution: Experience Manager
title: 設定ファイル
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 設定ファイル{#configuration-files}

画像レンダリングの設定は、Platform Serverの設定ファイルに保存されます。

プラットフォームサーバー設定ファイルは、[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]にあります。 このファイルは、JAVAプロパティファイルです。 適切な規則に従うように注意する必要があります。そうしないと、Platform Serverの起動に失敗する可能性があります。 このタイプのファイルではバックスラッシュがエスケープ文字として使用されるので、Windowsのファイルパスでは、単純なバックスラッシュ(\)の代わりに、バックスラッシュ(`\\`)またはスラッシュ(/)を1つ使用する必要があります。 ファイルには、ドキュメントに記載されていないプロパティが含まれています。このプロパティは内部サーバーでの使用用であり、変更することはできません。

すべての画像レンダリング設定のリストについては、 [設定設定リファレンス](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)を参照してください。
