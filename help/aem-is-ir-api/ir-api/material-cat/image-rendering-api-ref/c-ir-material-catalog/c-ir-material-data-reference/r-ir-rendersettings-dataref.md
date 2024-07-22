---
description: レンダリングの詳細設定 高度なレンダリング設定は、マテリアルのシャープ処理のタイプやパラメータ、照明アルゴリズムの特定のパラメータなど、レンダリング エンジンの低レベルな側面を制御するために使用します。
solution: Experience Manager
title: RenderSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37b806f8-e314-4532-a28c-1cc4ab939f09
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# RenderSettings{#rendersettings}

レンダリングの詳細設定 高度なレンダリング設定は、マテリアルのシャープ処理のタイプやパラメータ、照明アルゴリズムの特定のパラメータなど、レンダリング エンジンの低レベルな側面を制御するために使用します。

## プロパティ {#section-b4c8fe595efc4838ac598659bc820607}

テキスト文字列 すべてのマテリアルに対してオプションです。 指定する場合は、Dynamic Media画像オーサリングツール（Vignette Image Authoring パッケージの一部）で定義された有効なレンダリング設定文字列である必要があります。

## 初期設定 {#section-6a4d2013c1d34284b4ff21bb07485d28}

指定しない場合は `attribute::RenderSettings`、空の場合は空です。

## 関連項目 {#section-52679fc35c36439490564b4d1c515dd0}

[rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)、[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0)、[attribute::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd)
