---
title: SynthesizeFontStyles
description: 合成フォントのバリエーションを有効にします。 サーバーがエラー応答を生成するか、または太字、斜体、太字/斜体のフォント スタイルを要求したがフォント マップに見つからない場合に、そのスタイルを合成するかを制御します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# SynthesizeFontStyles{#synthesizefontstyles}

合成フォントのバリエーションを有効にします。 サーバーがエラー応答を生成するか、または太字、斜体、太字/斜体のフォント スタイルを要求したがフォント マップに見つからない場合に、そのスタイルを合成するかを制御します。

>[!NOTE]
>
>多くの場合、フォントスタイルを合成すると、そのようなスタイルに実際のフォントを使用するよりもレンダリングの品質が低下します。

## プロパティ {#section-3205560a74774ebf9c916b07bd15aca6}

フラグ。 0 に設定すると無効になり、1 に設定すると合成フォントスタイルが有効になります。

## 初期設定 {#section-71f94aa65e404d14b441674c040b59e3}

定義されていない場合または空の場合は `default::SynthesizeFontStyles` から継承します。

## 関連項目 {#section-47a79659cc844272b6d5f36c946e12ac}

[フォントマップの参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
