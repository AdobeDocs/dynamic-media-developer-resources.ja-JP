---
description: SvgRenderコンポーネントは、独立したJavaアプリケーションです。
solution: Experience Manager
title: SVGの設定
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 2%

---


# SVG{#configuring-svg}の設定

SvgRenderコンポーネントは、独立したJavaアプリケーションです。

SVG設定は、[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]、[!DNL ServerSupervisorRegistry.xml]にあります。

ソケット接続は、SvgRenderとImage Server間の通信に使用されます。 ポート番号は27346です。 必要に応じて、[!DNL svg.conf]の`SVGRender.port`と[!DNL ImageServerRegistry.xml]の`<SVGTcpPort>`を新しい値に設定することで変更できます。

## 関連項目 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
