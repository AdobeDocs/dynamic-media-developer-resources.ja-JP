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

---


# SVGの設定{#configuring-svg}

SvgRenderコンポーネントは、独立したJavaアプリケーションです。

SVG設定は、、、およびにあ [!DNL PlatformServer.conf]り [!DNL SVG.conf]ます [!DNL ImageServerRegistry.xml][!DNL ServerSupervisorRegistry.xml]。

ソケット接続は、SvgRenderとImage Serverの間の通信に使用されます。 ポート番号は27346です。 必要に応じて、にを設定し、新しい値 `SVGRender.port` にを設 [!DNL svg.conf] 定し `<SVGTcpPort>` て変更 [!DNL ImageServerRegistry.xml] できます。

## 関連項目 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
