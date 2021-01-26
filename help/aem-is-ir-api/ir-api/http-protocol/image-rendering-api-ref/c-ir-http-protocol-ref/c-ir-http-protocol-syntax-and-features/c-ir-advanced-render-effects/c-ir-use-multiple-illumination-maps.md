---
description: アプリケーションによっては、異なる種類のマテリアルに対して異なる照明マップが必要になる場合があります。
seo-description: アプリケーションによっては、異なる種類のマテリアルに対して異なる照明マップが必要になる場合があります。
seo-title: 複数の照明マップの使用
solution: Experience Manager
title: 複数の照明マップの使用
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# 複数の照明マップを使用する{#using-multiple-illumination-maps}

アプリケーションによっては、異なる種類のマテリアルに対して異なる照明マップが必要になる場合があります。

各ビネットに対して最大3つの照明マップをオーサリングできます。 レンダリング操作の照明マップは、`illum=`コマンドまたは`gloss=`コマンドを使用して選択されます。

**既定の** 選択ま `illum=` たは `gloss=` 指定されていない場合、レンダラーは最初に作成した照明マップ（通常はマップA、&#39;Flat&#39;照明マップ）を使用します。

**自動選択(`gloss=`** 指定なし) `illum=` または —1に設定した場合、レンダラーは指定した `gloss=` 値とビネット内の各照明マップに関連付けられた光沢値を比較し、指定した値に最も光沢値が近い照明マップを選択し `gloss=`ます。

**[明示的な選択]`illum=`** を指定 `illum=` し、0、1、または2に設定した場合、レンダラーは対応する照明マップを使用します。 `gloss=` は、イルミネーションマップを選択する目的で無視されます。

ビネットに照明マップが1つしか含まれていない場合、レンダラーはそのマップを使用し、`illum=`および`gloss=`コマンドは無視します。
