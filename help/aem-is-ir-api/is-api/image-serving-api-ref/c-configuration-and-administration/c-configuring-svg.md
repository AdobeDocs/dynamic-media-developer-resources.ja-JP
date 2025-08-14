---
description: SvgRender コンポーネントは独立した Java アプリケーションです。
solution: Experience Manager
title: SVGの設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# SVGの設定{#configuring-svg}

SvgRender コンポーネントは独立した Java アプリケーションです。

SVGの設定は、[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml] および [!DNL ServerSupervisorRegistry.xml] にあります。

ソケット接続は、SvgRender と Image Server 間の通信に使用されます。 ポート番号は 27346 です。 必要に応じて、`SVGRender.port` に [!DNL svg.conf]、`<SVGTcpPort>` に [!DNL ImageServerRegistry.xml] を新しい値に設定して変更できます。

## 関連項目 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVGの設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
