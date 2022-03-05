---
title: 複数のイルミネーションマップの使用
description: 一部の用途では、異なる種類のマテリアルに対して異なる照明マップが必要になる場合があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 複数のイルミネーションマップの使用{#using-multiple-illumination-maps}

一部の用途では、異なる種類のマテリアルに対して異なる照明マップが必要になる場合があります。

各ビネットに対して最大 3 つの照明マップを作成できます。 レンダリング操作のイルミネーションマップは、 `illum=` およびまたは `gloss=` コマンド

**デフォルトの選択** - If `illum=` または `gloss=` が指定されていない場合、レンダラーは最初に作成した照明マップ（通常はマップ A、「フラット」照明マップ）を使用します。

**自動選択`gloss=`** - If `illum=` が指定されていないか、に設定されています `-1`を指定した場合、レンダラーは指定した `gloss=` value は、ビネットの各照明マップに関連付けられた光沢値を持ちます。 指定した値に最も光沢値が近い照明マップを選択します。 `gloss=`.

**を使用した明示的な選択`illum=`** - If `illum=` が指定され、に設定されている `0`, `1`または `2`を指定した場合、レンダラは対応するイルミネーションマップを使用します。 `gloss=` は、イルミネーションマップを選択する際に無視されます。

ビネットに 1 つのイルミネーションマップのみが含まれている場合、レンダラーはそのマップを使用し、 `illum=` および `gloss=` コマンド
