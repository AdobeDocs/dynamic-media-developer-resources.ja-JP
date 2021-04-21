---
description: 合成フォントのバリエーションを有効にする。 エラー応答を生成するか、太字、斜体、太字/斜体のフォントスタイルが要求されたがフォントマップに見つからない場合に、サーバーがそのスタイルを合成するかを制御します。
solution: Experience Manager
title: SyntesizeFontStyles
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# SyntesizeFontStyles{#synthesizefontstyles}

合成フォントのバリエーションを有効にする。 エラー応答を生成するか、太字、斜体、太字/斜体のフォントスタイルが要求されたがフォントマップに見つからない場合に、サーバーがそのスタイルを合成するかを制御します。

>[!NOTE]
>
>フォントスタイルを合成すると、そのようなスタイルで実際のフォントを使用する場合よりも、レンダリングの品質が低くなることがよくあります。

## プロパティ {#section-3205560a74774ebf9c916b07bd15aca6}

フラグ。 0に設定すると無効になり、1に設定すると合成フォントスタイルが有効になります。

## 初期設定 {#section-71f94aa65e404d14b441674c040b59e3}

定義されていない場合や空の場合は`default::SynthesizeFontStyles`から継承されます。

## 関連項目 {#section-47a79659cc844272b6d5f36c946e12ac}

[フォントマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
