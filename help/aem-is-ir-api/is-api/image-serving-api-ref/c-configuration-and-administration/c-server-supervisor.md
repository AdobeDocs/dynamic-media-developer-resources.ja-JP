---
description: 画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス(S7Supervisor.exe、サービスCampaign コントロールパネルで「Scene7画像サービング」と表示)であるサーバスーパバイザによって管理されます。
seo-description: 画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス(S7Supervisor.exe、サービスCampaign コントロールパネルで「Scene7画像サービング」と表示)であるサーバスーパバイザによって管理されます。
seo-title: サーバースーパーバイザ
solution: Experience Manager
title: サーバースーパーバイザ
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# サーバのスーパーバイザ{#server-supervisor}

画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス(S7Supervisor.exe、サービスCampaign コントロールパネルで「Scene7画像サービング」と表示)であるサーバスーパバイザによって管理されます。

サーバスーパーバイザは、他の画像サービングコンポーネントの起動と停止に加え、他のコンポーネントの正常性を確保する役割を担います。 コンポーネントがクラッシュした場合は、サービスの中断を最小限に抑えるために自動的に再起動されます。

## {#section-061d28d74e034a30adc39ea3e2031cd0}の開始と停止

サーバスーパーバイザは、Image Serving Utilityスクリプトを使用して起動、停止および再起動します。 詳しくは、[ユーティリティのドキュメント](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)を参照してください。

サーバスーパーバイザの起動と停止は、自動的に開始を行い、他のすべてのイメージサービングコンポーネントを停止します。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
