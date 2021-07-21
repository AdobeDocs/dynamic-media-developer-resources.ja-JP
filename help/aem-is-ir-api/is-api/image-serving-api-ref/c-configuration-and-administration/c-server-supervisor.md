---
description: 画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス(S7Supervisor.exe、サービスCampaign コントロールパネルには「Dynamic Media Image Serving」と表示)であるServer Supervisorによって管理されます。
solution: Experience Manager
title: サーバスーパーバイザ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# サーバスーパーバイザ{#server-supervisor}

画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス(S7Supervisor.exe、サービスCampaign コントロールパネルには「Dynamic Media Image Serving」と表示)であるServer Supervisorによって管理されます。

サーバスーパーバイザは、他の画像サービングコンポーネントの起動と停止に加えて、他のコンポーネントのヘルスを確保する役割を担います。 コンポーネントがクラッシュした場合は、サービスの中断を最小限に抑えるために、自動的に再起動されます。

## 開始と停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

Image Servingユーティリティスクリプトを使用して、サーバスーパーバイザを起動、停止、および再起動します。 詳しくは、[ユーティリティのドキュメント](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)を参照してください。

サーバスーパーバイザの起動と停止は、他のすべての画像サービングコンポーネントを自動的に起動および停止します。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
