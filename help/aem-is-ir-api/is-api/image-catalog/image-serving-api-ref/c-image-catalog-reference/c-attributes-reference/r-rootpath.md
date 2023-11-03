---
description: ソースデータのルートパス。 この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# RootPath{#rootpath}

ソースデータのルートパス。 この画像カタログのソースデータのルートフォルダーの絶対パスまたは相対パス。

The `RootPath` はテキスト文字列値です。 詳しくは、 [ソースデータの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) を参照してください。

## プロパティ {#section-b41d7e0ea63143eb8034569706cad0c0}

テキスト文字列。 空、有効な相対フォルダーパス、または Image Server からアクセス可能な有効な絶対パスを指定する必要があります。

## 初期設定 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

継承元 `default::RootPath` （定義されていない場合） 定義されているが空の場合、ソースファイルのルートパスには影響しません。

## 関連項目 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [ソースデータの管理](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
