---
description: ソースデータのルートパス この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。
seo-description: ソースデータのルートパス この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。
seo-title: RootPath
solution: Experience Manager
title: RootPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 859bebf2-5ee7-4daa-8970-a18bddcee684
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# RootPath{#rootpath}

ソースデータのルートパス この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。

はテキ `RootPath` スト文字列値です。 サーバー [のルートパスの詳細については](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) 、「Managing Source Data」を参照してください。

## プロパティ {#section-b41d7e0ea63143eb8034569706cad0c0}

テキスト文字列。 空、有効な相対フォルダパス、またはImage Serverがアクセス可能な有効な絶対パスである必要があります。

## 初期設定 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

定義されていな `default::RootPath` い場合は、から継承。 定義済みで空の場合、はソースファイルのルートパスに影響しません。

## 関連項目 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) 、 [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)、 [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)、ソースデ [ータの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
