---
description: SvgRenderコンポーネントは、独立したJavaアプリケーションです。
seo-description: SvgRenderコンポーネントは、独立したJavaアプリケーションです。
seo-title: SVGの設定
solution: Experience Manager
title: SVGの設定
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 2%

---


# SVG{#configuring-svg}の設定

SvgRenderコンポーネントは、独立したJavaアプリケーションです。

SVG設定は、[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]、[!DNL ServerSupervisorRegistry.xml]にあります。

ソケット接続は、SvgRenderとImage Server間の通信に使用されます。 ポート番号は27346です。 必要に応じて、[!DNL svg.conf]の`SVGRender.port`と[!DNL ImageServerRegistry.xml]の`<SVGTcpPort>`を新しい値に設定することで変更できます。

## 関連項目 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
