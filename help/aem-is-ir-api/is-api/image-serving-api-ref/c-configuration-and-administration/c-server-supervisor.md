---
description: 画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス（S7Supervisor.exe、コントロールパネルの「Scene7 Image Serving」と表示）であるServer Supervisorで管理されます。
seo-description: 画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス（S7Supervisor.exe、コントロールパネルの「Scene7 Image Serving」と表示）であるServer Supervisorで管理されます。
seo-title: サーバの管理者
solution: Experience Manager
title: サーバの管理者
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# サーバの管理者{#server-supervisor}

画像サービングコンポーネントは、LinuxデーモンまたはWindowsサービス（S7Supervisor.exe、コントロールパネルの「Scene7 Image Serving」と表示）であるServer Supervisorで管理されます。

サーバスーパーバイザは、他の画像サービングコンポーネントの起動と停止に加えて、これらの他のコンポーネントの正常性を確保します。 コンポーネントがクラッシュした場合は、サービスの中断を最小限に抑えるために自動的に再起動されます。

## 開始と停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

サーバスーパーバイザは、画像サービングユーティリティスクリプトを使用して起動、停止および再起動します。 See the [Utilities documentation](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) for more information.

サーバスーパーバイザの起動と停止は、他のすべての画像サービングコンポーネントを自動的に起動および停止します。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
