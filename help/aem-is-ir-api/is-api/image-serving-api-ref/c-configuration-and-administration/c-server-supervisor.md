---
description: 画像サービングコンポーネントは、サーバースーパーバイザー（Linux デーモンまたは Windows サービスの 1 つ）によって管理されます（S7Supervisor.exe は、サービスCampaign コントロールパネルで「Dynamic Media 画像サービング」と表示されます）。
solution: Experience Manager
title: サーバースーパーバイザー
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# サーバースーパーバイザー{#server-supervisor}

画像サービングコンポーネントは、サーバースーパーバイザー（Linux デーモンまたは Windows サービスの 1 つ）によって管理されます（S7Supervisor.exe は、サービスCampaign コントロールパネルで「Dynamic Media 画像サービング」と表示されます）。

サーバースーパーバイザーは、他の画像サービングコンポーネントの起動と停止に加えて、これらの他のコンポーネントの正常性を確保する役割を担います。 コンポーネントがクラッシュした場合は、サービスの中断を最小限に抑えるために自動的に再起動されます。

## 起動と停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

Server Supervisor が起動、停止、およびイメージ サービング ユーティリティ スクリプトを使用して再起動されます。 詳しくは、[ ユーティリティのドキュメント ](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) を参照してください。

サーバースーパーバイザーを起動および停止すると、他のすべての画像サービングコンポーネントが自動的に起動および停止します。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
