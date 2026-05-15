---
description: SvgRender コンポーネントは、独立したJava アプリケーションです。
solution: Experience Manager
title: SVGの設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
TQID: 'https://experienceleague.adobe.com/e6eoh1OQJoWFv0-C1xQTqygrGY4Z7m6IkefFblj-yuE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 3%

---

# SVGの設定{#configuring-svg}

SvgRender コンポーネントは、独立したJava アプリケーションです。

SVGの設定は[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]、[!DNL ServerSupervisorRegistry.xml]にあります。

ソケット接続は、SvgRenderとImage Server間の通信に使用されます。 ポート番号は27346です。 必要に応じて、[!DNL svg.conf]の`SVGRender.port`と[!DNL ImageServerRegistry.xml]の`<SVGTcpPort>`を新しい値に設定することで変更できます。

## 関連項目 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVGの設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
