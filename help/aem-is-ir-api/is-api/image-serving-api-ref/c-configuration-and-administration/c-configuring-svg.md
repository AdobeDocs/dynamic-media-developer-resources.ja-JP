---
description: SvgRenderコンポーネントは、独立したJavaアプリケーションです。
solution: Experience Manager
title: SVGの設定
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# SVGの設定{#configuring-svg}

SvgRenderコンポーネントは、独立したJavaアプリケーションです。

SVG設定は、[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]および[!DNL ServerSupervisorRegistry.xml]にあります。

ソケット接続は、SvgRenderとImage Server間の通信に使用されます。 ポート番号は27346です。 必要に応じて、[!DNL svg.conf]に`SVGRender.port`を、[!DNL ImageServerRegistry.xml]に`<SVGTcpPort>`を新しい値に設定して変更できます。

## 関連項目 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
