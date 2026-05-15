---
title: SynthesizeFontStyles
description: 合成されたフォントバリエーションを有効にします。 サーバーがエラー応答を生成するか、太字、斜体、太字/斜体のフォントスタイルを合成するかを制御します。このようなスタイルが要求されますが、フォントマップに見つからない場合です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
TQID: 'https://experienceleague.adobe.com/E5yyjiqiPxEbLecNDw5HIa3dJ9XqyGa3Ipys4EtancU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# SynthesizeFontStyles{#synthesizefontstyles}

合成されたフォントバリエーションを有効にします。 サーバーがエラー応答を生成するか、太字、斜体、太字/斜体のフォントスタイルを合成するかを制御します。このようなスタイルが要求されますが、フォントマップに見つからない場合です。

>[!NOTE]
>
>フォントスタイルを合成すると、多くの場合、そのようなスタイルに実際のフォントを使用するよりも画質の低いレンダリングになります。

## プロパティ {#section-3205560a74774ebf9c916b07bd15aca6}

フラグ： 0に設定すると無効になり、1に設定すると合成フォントスタイルが有効になります。

## 初期設定 {#section-71f94aa65e404d14b441674c040b59e3}

定義されていない場合や空の場合は、`default::SynthesizeFontStyles`から継承されます。

## 関連項目 {#section-47a79659cc844272b6d5f36c946e12ac}

[フォントマップ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
