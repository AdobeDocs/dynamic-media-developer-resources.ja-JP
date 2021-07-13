---
description: ソースデータのルートパス。 この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# RootPath{#rootpath}

ソースデータのルートパス。 この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。

`RootPath`はテキスト文字列値です。 サーバーのルートパスの詳細については、「[ソースデータの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)」を参照してください。

## プロパティ {#section-b41d7e0ea63143eb8034569706cad0c0}

テキスト文字列。 空、有効な相対フォルダーパス、またはImage Serverがアクセス可能な有効な絶対パスである必要があります。

## 初期設定 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

定義されていない場合は`default::RootPath`から継承されます。 定義されているが空の場合、はソースファイルのルートパスに影響しません。

## 関連項目 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) 、 [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)、  [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)、ソースデータの [管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
