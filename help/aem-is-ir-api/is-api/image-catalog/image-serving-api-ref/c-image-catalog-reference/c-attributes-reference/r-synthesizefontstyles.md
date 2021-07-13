---
description: 合成フォントのバリエーションを有効にします。 サーバーがエラー応答を生成するか、太字、斜体、太字/斜体のフォントスタイルを合成するかを制御します（このスタイルが要求されたが、フォントマップに見つからない場合）。
solution: Experience Manager
title: SyntesifyFontStyles
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# SyntesifyFontStyles{#synthesizefontstyles}

合成フォントのバリエーションを有効にします。 サーバーがエラー応答を生成するか、太字、斜体、太字/斜体のフォントスタイルを合成するかを制御します（このスタイルが要求されたが、フォントマップに見つからない場合）。

>[!NOTE]
>
>フォントスタイルを合成すると、多くの場合、そのようなスタイルで実際のフォントを使用するよりも低画質でレンダリングされます。

## プロパティ {#section-3205560a74774ebf9c916b07bd15aca6}

フラグ。 0に設定すると無効になり、1に設定すると合成フォントスタイルが有効になります。

## 初期設定 {#section-71f94aa65e404d14b441674c040b59e3}

`default::SynthesizeFontStyles`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-47a79659cc844272b6d5f36c946e12ac}

[フォントマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
